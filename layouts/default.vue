<template>
  <v-app>
    <v-navigation-drawer class="tw-text-black" color=#ffffff :mini-variant="miniVariant" :clipped="clipped" fixed permanent app>
      <v-list>
        <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:javascript" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono right-ml">Javascript</h1>
        </v-list-item>
        <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:sass" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">SASS</h1>
        </v-list-item>
        <v-list-item class="tw-cursor-pointer">
          <Icon icon="vscode-icons:file-type-tailwind" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">Tailwindcss</h1>
        </v-list-item>
        <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:vue" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">Vue</h1>
        </v-list-item>
        <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:nuxt-icon" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">NuxtJS</h1>
        </v-list-item>
       <v-list-item class="tw-cursor-pointer">
            <Icon icon="logos:python" color="lime" class="tw-text-3xl" />
            <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">Python</h1> </v-list-item
          ><v-list-item class="tw-cursor-pointer">
            <Icon icon="logos:nodejs-icon" color="lime" class="tw-text-3xl" />
            <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">NodeJS</h1>
          </v-list-item>
          <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:docker-icon" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">Docker</h1>
        </v-list-item>
        <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:postgresql" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">Postgres</h1>
        </v-list-item>
        <v-list-item class="tw-cursor-pointer">
          <Icon icon="vscode-icons:file-type-mongo" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">MongoDB</h1>
        </v-list-item>
           <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:git-icon" color="lime" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">Git </h1>
        </v-list-item>
         <v-list-item class="tw-cursor-pointer">
          <Icon icon="logos:aws" color="white" class="tw-text-3xl" />
          <h1 class="tw-ml-4 tw-text-black tw-font-bolder tw-font-mono">Amazon Web Services</h1>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-apps</v-icon>
      </v-btn>
        <v-btn>      <v-toolbar-title v-text="title" @click="$nuxt.$router.push('/skills')" />
    </v-btn>
  <v-spacer />
   <v-btn @click="$nuxt.$router.push('/')">
        <v-icon>mdi-home</v-icon>
      </v-btn>
      <v-btn @click="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-application</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed color=#ffffff>
    <h1 class="tw-text-2xl tw-text-bold tw-text-black tw-underline tw-m-4 ">Experiencia</h1>
     
      <v-list>
        <v-list-item>
           <div>
          <h1 class="tw-my-8 tw-text-black tw-font-bolder tw-font-cursive tw-underline tw-text-md">Bluetab an IBM Company</h1>
          <img src="/bluetab.svg"/>
          <h2 class="tw-text-green-700 text-md">Data Developer</h2></div>
          </v-list-item>
        <v-list-item>
          <div>
          <h1 class="tw-my-8 tw-text-black tw-font-bolder tw-font-cursive tw-underline tw-text-md">Indra Company</h1>
          <img src="/indra.png">
          <h2 class="tw-text-green-700 text-md">Data Engineer</h2>
          </div>
          </v-list-item>
        <v-list-item>
          <div>
          <h1 class="tw-my-8 tw-text-black tw-font-bolder tw-font-cursive tw-underline tw-text-md">Valtx</h1>
          <img src="valtx.png" />
          <h2 class="tw-text-green-700 text-md">IT Analyst</h2>
          </div>
          </v-list-item>
        <v-list-item>
          <div>
          <h1 class="tw-my-8 tw-text-black tw-font-bolder tw-font-cursive tw-underline tw-text-md">Telefonica</h1>
          <img src="/telefonica.png" />
          <h2 class="tw-text-green-700 text-md">Presales Engineer</h2>
          </div>
          </v-list-item>
        <v-list-item>
          <div>
          <h1 class="tw-my-8 tw-text-black tw-font-bolder tw-font-cursive tw-underline tw-text-md">Huawei</h1>
          <img src="/huawei.png" />
          <h2 class="tw-text-green-700 text-md">Services Engineer</h2>
          </div>
          </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app>
      <span
        >Designed and Developed by Oscar Bahamonde &copy;
        {{ new Date().getFullYear() }}</span
      >
      <div class="tw-ml-24">
        <v-btn circle mdi icon color="secondary" class="tw-bg-blue-700 tw-p-1 mx-4 tw-m-1"
          ><v-icon>mdi-linkedin</v-icon></v-btn
        ><v-btn
          circle
          mdi
          icon
          color="secondary"
          class="tw-bg-white tw-p-1 tw-m-1 mx-4 hover:scale-125"
          ><v-icon>mdi-github</v-icon></v-btn
        >
        <v-btn
          circle
          mdi
          icon
          color="secondary"
          class="tw-bg-pink-300 tw-p-1 mx-4 tw-m-1 hover:scale-125"
          ><v-icon>mdi-codepen</v-icon></v-btn
        >
        <v-btn
          circle
          mdi
          icon
          color="secondary"
          class="tw-bg-red-700 tw-p-1 mx-4 tw-m-1 hover:scale-125"
          ><v-icon>mdi-youtube</v-icon></v-btn
        >
        <v-btn
          circle
          mdi
          icon
          color="secondary"
          class="tw-bg-blue-300 tw-p-1 mx-4 tw-m-1 hover:scale-125"
          ><v-icon>mdi-twitter</v-icon></v-btn
        >
        <v-btn
          circle
          mdi
          icon
          color="secondary"
          class="tw-bg-green-500 tw-p-1 mx-4 tw-m-1 hover:scale-125"
          ><v-icon>mdi-whatsapp</v-icon></v-btn
        >
      </div>
    </v-footer>
  </v-app>
</template>

<script>
import { Icon } from "@iconify/vue2";
export default {
  name: "DefaultLayout",
  components: {
    Icon,
  },
  data() {
    return {
      clipped: true,
      drawer: true,
      fixed: false,
      miniVariant: true,
      right: true,
      rightDrawer: false,
      title: "Skills",
    };
  },
};
</script>
