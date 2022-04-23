<template>
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
    name="submitForm"
    data-netlify="true"
    data-netlify-honeypot="bot-field"
    method="POST"
    @submit.prevent="onSubmit"
  >
    <input type="hidden" name="form-name" value="submitForm" />
    <v-text-field
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="Tu nombre"
      required
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="Tu E-mail"
      required
    ></v-text-field>

    <textarea
      v-model="text"
      :rules="messageRules"
      label="Text"
      required
      placeholder="Tu mensaje"
      class="tw-w-full tw-bg-slate-700 tw-rounded tw-p-4"
    ></textarea>

    <v-checkbox
      v-model="checkbox"
      :rules="[v => !!v || 'Debes aceptar para continuar']"
      label="Acepto recibir información y contenido exclusivo gratis"
      required
    ></v-checkbox>

    <v-btn
      type="submit"
      :disabled="!valid"
      color="success"
      class="mr-4"
      @click="validate"
      outlined
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
      checkbox: true,
      name: '',
      nameRules: [
        v => !!v || 'Tu nombre es requerido',
        v => (v && v.length <= 32) || 'El nombre no puede tener más de 32 caracteres',
      ],
      email: '',
      emailRules: [
        v => !!v || 'Debes colocar tu E-mail',
        v => /.+@.+\..+/.test(v) || 'Debes colocar un E-mail válido',
      ],
      text: '',
      textRules: [
        v => !!v || 'Debes dejar un mensaje',
        v => (v && v.length <= 256) || 'El mensaje debe tener menos de 256 caracteres',
      ],
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
     onSubmit () {
       alert('Formulario enviado')
     }
    }
  }
</script>