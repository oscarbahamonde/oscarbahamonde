<template>
  <v-row justify="center" align="center" style="background-color: #121212"  >
    <v-col cols="12" sm="2" md="3">Hello</v-col>
    <v-col cols="12" sm="8" md="6">
      
      <v-card class="tw-shadow-lg" >
        <h1 class="tw-m-4 tw-text-2xl tw-text-center">
          Bienvenidos a mi web personal soy Oscar Bahamonde y les presento mi CV online.
        </h1>
        <v-card class="tw-w-3/4 logo py-4 d-flex tw-justify-center tw-ml-16 tw-shadow-lg" color="#ccc">
        <VuetifyLogo />
      </v-card>
        <v-card-text>
          <p>
            Soy ingeniero de telecomunicaciones ejerciendo las disciplinas de Cloud
            Computing, Ingenieria de Datos y Desarrollo de software motivado por la curiosidad genuina y mis
            ganas de salir de la zona de confort, estoy constantemente aprendiendo y
            tratando de ser mejor cada día.
          </p>
          <p>
            Para mayor información sobre mi hoja de vida puedes consultar mi 
            <a href="/resume" target="_blank" rel="noopener noreferrer"> Currículum </a> en pdf.
          </p>
          <p>
            Si tienes alguna duda o interés en mi trabajo me puedes contactar al correo
            mediante
            <button nuxt to="/contact">este Formulario</button>
          </p>
        </v-card-text>
        <v-card-text>
          <p class="px-4 font-italic">
            Gracias por visitar mi perfil, recuerda que no hay mejor manera de aprender efectivamente algo
             que enseñando lo poco que ya sabes.
          </p>
          <div class="text-xs-right px-4">
            <em><small>&mdash; Oscar Bahamonde</small></em>
          </div>
          <hr class="my-3" />
          <br />
          <v-btn elevation="10" nuxt to="/portfolio" color="primary" class="tw-mx-2 tw-ml-4 tw-text-sm"><Icon icon="emojione-v1:briefcase" class="tw-mr-1 tw-mb-1 tw-text-sm" />Portfolio</v-btn><v-btn elevation="10" nuxt to="/contact" color="primary" class="tw-mx-4"><Icon icon="emojione-v1:envelope" class="tw-mr-1 tw-mb-1 tw-text-sm" />Contact</v-btn><v-btn elevation="10" nuxt to="/services" color="primary" class="tw-mx-2 tw-text-sm"><Icon icon="logos:visual-studio-code" class="tw-mr-1 tw-mb-1 tw-text-sm" />Services</v-btn>
          <br />
        </v-card-text>
      </v-card>
    </v-col>
      <v-col cols="12" sm="2" md="3">Hello</v-col>
  </v-row>
</template>

<script>
import { Icon } from '@iconify/vue2'
export default {
  components: {
    Icon
  },
  name: "IndexPage",
};
</script>