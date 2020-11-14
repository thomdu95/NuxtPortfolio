<template>
  <div class="myContainer contactContainer">
    <v-alert
      v-if="success"
      dense
      text
      type="success"
    >
      Votre email a bien été transmis à <strong>Thomas Jamais</strong>. Merci de votre message !
    </v-alert>
    <v-alert
      v-if="error"
      dense
      outlined
      type="error"
    >
      Votre email n'a pas pu être transmit à <strong>Thomas Jamais</strong>, merci de re essayer plus tard !
    </v-alert>
    <h3 class="textImportant">
      Prise de contact
    </h3>
    <form class="contactForm">
      <v-text-field
        v-model="name"
        :error-messages="nameErrors"
        :counter="35"
        label="Votre Nom"
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
      />
      <v-text-field
        v-model="email"
        :error-messages="emailErrors"
        label="Votre E-mail"
        required
        @input="$v.email.$touch()"
        @blur="$v.email.$touch()"
      />
      <Editor :change-content="changeContent" />
      <v-btn class="mr-4 mt-10" @click="submit">
        Envoyer
      </v-btn>
      <v-btn class="mt-10" @click="clear">
        Réinitialiser
      </v-btn>
    </form>
  </div>
</template>

<script>
import { validationMixin } from 'vuelidate'
import { required, maxLength, email } from 'vuelidate/lib/validators'
import Editor from '~/components/Editor'

export default {
  components: { Editor },
  mixins: [validationMixin],

  validations: {
    name: { required, maxLength: maxLength(35) },
    email: { required, email }
  },

  data: () => ({
    name: '',
    email: '',
    message: '',
    error: false,
    success: false
  }),

  computed: {
    nameErrors () {
      const errors = []
      if (!this.$v.name.$dirty) { return errors }
      !this.$v.name.maxLength &&
        errors.push('Votre Nom de peu avoir que 35 characteres maximum.')
      !this.$v.name.required && errors.push('Votre nom est requis.')
      return errors
    },
    emailErrors () {
      const errors = []
      if (!this.$v.email.$dirty) { return errors }
      !this.$v.email.email && errors.push('Votre e-mail doit être valide')
      !this.$v.email.required && errors.push('L\'email est requis')
      return errors
    }
  },

  methods: {
    submit () {
      this.$v.$touch()
      if (!this.$v.error) {
        const toSend = {
          name: this.name,
          email: this.email,
          message: this.message
        }
        this.$axios.post('https://emailthomasjamais.herokuapp.com/sendEmail', toSend)
          .then((response) => {
            this.error = false
            this.success = true
            return response
          })
          .catch((error) => {
            if (error) {
              this.success = false
              this.error = true
            }
          })
      }
    },
    clear () {
      this.$v.$reset()
      this.name = ''
      this.email = ''
      this.message = ''
    //   this.select = null
    //   this.checkbox = false
    },
    changeContent (content) {
      this.message = content
    }
  }
}
</script>

<style>
.contactForm {
    width: 80%;
}

.contactContainer {
    background-color: #e3e3e3;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='60' height='60' viewBox='0 0 200 200'%3E%3Cpolygon fill='%23fafafa' fill-opacity='0.39' points='100 0 0 100 100 100 100 200 200 100 200 0'/%3E%3C/svg%3E");
    background-attachment: fixed;
    background-repeat: initial;
}

@media only screen and (max-width: 600px) {
  .contactContainer {
    padding: 20vh 0;
  }
}
</style>
