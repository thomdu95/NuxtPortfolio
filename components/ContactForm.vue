<template>
  <div class="myContainer contactContainer">
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
      <!-- <v-select
        v-model="select"
        :items="items"
        :error-messages="selectErrors"
        label="Item"
        required
        @change="$v.select.$touch()"
        @blur="$v.select.$touch()"
      />
      <v-checkbox
        v-model="checkbox"
        :error-messages="checkboxErrors"
        label="Do you agree?"
        required
        @change="$v.checkbox.$touch()"
        @blur="$v.checkbox.$touch()"
      /> -->

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
    // select: { required },
    // checkbox: {
    //   checked (val) {
    //     return val
    //   }
    // }
  },

  data: () => ({
    name: '',
    email: '',
    message: ''
    // select: null,
    // items: ['Item 1', 'Item 2', 'Item 3', 'Item 4'],
    // checkbox: false
  }),

  computed: {
    // checkboxErrors () {
    //   const errors = []
    //   if (!this.$v.checkbox.$dirty) { return errors }
    //   !this.$v.checkbox.checked && errors.push('You must agree to continue!')
    //   return errors
    // },
    // selectErrors () {
    //   const errors = []
    //   if (!this.$v.select.$dirty) { return errors }
    //   !this.$v.select.required && errors.push('Item is required')
    //   return errors
    // },
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
    },
    clear () {
      this.$v.$reset()
      this.name = ''
      this.email = ''
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
</style>
