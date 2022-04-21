<template>
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
    name="submitForm"
    data-netlify="true"
    data-netlify-honeypot="bot-field"
    method="POST"
  >
    <input type="hidden" name="form-name" value="submitForm" />
    <v-text-field
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="Name"
      required
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
    ></v-text-field>

    <textarea
      v-model="text"
      :rules="messageRules"
      label="Text"
      required
      placeholder="write your message here"
      class="tw-w-full tw-bg-slate-700 tw-rounded tw-p-4"
    ></textarea>

    <v-checkbox
      v-model="checkbox"
      :rules="[v => !!v || 'You must agree to continue!']"
      label="Do you agree?"
      required
    ></v-checkbox>

    <v-btn
      :disabled="!valid"
      color="success"
      class="mr-4"
      @click="validate"
    >
      Submit
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset Form
    </v-btn>
  </v-form>
</template>
<script>
  export default {
    data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 32) || 'Name must be less than 32 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      text: '',
      textRules: [
        v => !!v || 'Message is required',
        v => (v && v.length <= 144) || 'Message must be less than 144 characters',
      ],
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
    },
  }
</script>