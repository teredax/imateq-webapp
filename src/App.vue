<template>
  <v-app>
    <v-app-bar
      app
      color="white"
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./assets/imateq.png"
          transition="scale-transition"
          width="200"
          @click="pushAndResetNav('/')"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>
      <v-btn @click="pushAndResetNav('/about')" text color="#0C5AA2" class="page-subtitle text-capitalize">
        <span>Quienes Somos</span>
      </v-btn>
      <v-btn @click="pushAndResetNav('/contact')" text color="#0C5AA2" class="text-capitalize page-subtitle">
        <span>Contacto</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <router-view/>
    </v-content>
    <v-layout row wrap px-10 style="background-color: #F6F6F6">
      <v-flex xs12>
        <v-divider horizontal></v-divider>
      </v-flex>
      <v-flex xs12 sm6 md4 text-center class="my-auto page-subtitle" py-10>
        <v-flex xs12>
          <v-icon large color="#0C5AA2">mdi-home</v-icon>
          <v-flex xs7 pt-2 class="mx-auto">
            <v-divider horizontal></v-divider>
          </v-flex>
        </v-flex>
        <v-flex xs12 pt-10>
          <p>16 de Septiembre #915 ote</p>
          <p>Col. Independencia, Monterrey, N.L.</p>
        </v-flex>
      </v-flex>
      <v-flex xs12 sm6 md4 text-center  class="my-auto page-subtitle" py-10>
        <v-flex xs12>
          <v-icon large color="#0C5AA2">mdi-phone</v-icon>
          <v-flex xs7 pt-2 class="mx-auto">
            <v-divider horizontal></v-divider>
          </v-flex>
        </v-flex>
        <v-flex xs12 pt-10>
          <v-flex xs12>
            <span>8190.4287</span>
          </v-flex>
          <v-flex xs12>
            <span>8114.3187</span>
          </v-flex>
          <v-flex xs12>
            <span>8114.3188</span>
          </v-flex>
        </v-flex>
      </v-flex>
      <v-flex xs12 sm6 md4 text-center class="mx-auto my-auto page-subtitle" py-10>
        <v-flex xs12>
          <v-icon large color="#0C5AA2">mdi-email</v-icon>
          <v-flex xs7 pt-2 class="mx-auto">
            <v-divider horizontal></v-divider>
          </v-flex>
        </v-flex>
        <v-flex xs12 pt-10>
          ventas@imateq.mx
        </v-flex>
        <v-flex xs12 pt-5>
          <v-btn tile depressed dark color="#0C5AA2">
            Contactanos
          </v-btn>
        </v-flex>
      </v-flex>
      <v-flex pt-10 xs12 text-center pt-2>
        <a style="text-decoration: none;"  href="https://www.facebook.com">
          <v-icon x-large color="#0C5AA2">mdi-facebook</v-icon>
        </a>
        <a style="text-decoration: none;"  href="https://www.instagram.com">
          <v-icon x-large color="#0C5AA2">mdi-instagram</v-icon>
        </a>
        <a style="text-decoration: none;"  href="https://www.whatsapp.com">
          <v-icon x-large color="#0C5AA2">mdi-whatsapp</v-icon>
        </a>
      </v-flex>
      <v-flex xs12 text-center class="page-subtitle">
        COPYRIGHT IMATEQ 2020 | ALL RIGHTS RESERVED
      </v-flex>
      <v-flex xs12>
        <v-divider horizontal></v-divider>
      </v-flex>
    </v-layout>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    //
  }),
  methods: {
    pushAndResetNav (route) {
      if (this.$route.path !== route) {
        this.$router.push(route)
      }
    }
  }
}
</script>

<style scoped>

@font-face {
  font-display: fallback;
  font-family: 'Poppins';
  src: url('./assets/fonts/Poppins-SemiBoldItalic.woff2') format('woff2'),
      url('./assets/fonts/Poppins-SemiBoldItalic.woff') format('woff');
  font-weight: 600;
  font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-ExtraBold.woff2') format('woff2'),
        url('./assets/fonts/Poppins-ExtraBold.woff') format('woff');
    font-weight: 800;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-Black.woff2') format('woff2'),
        url('./assets/fonts/Poppins-Black.woff') format('woff');
    font-weight: 900;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-LightItalic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-LightItalic.woff') format('woff');
    font-weight: 300;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-ExtraBoldItalic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-ExtraBoldItalic.woff') format('woff');
    font-weight: 800;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-ThinItalic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-ThinItalic.woff') format('woff');
    font-weight: 100;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-ExtraLight.woff2') format('woff2'),
        url('./assets/fonts/Poppins-ExtraLight.woff') format('woff');
    font-weight: 200;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-Regular.woff2') format('woff2'),
        url('./assets/fonts/Poppins-Regular.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-MediumItalic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-MediumItalic.woff') format('woff');
    font-weight: 500;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-Medium.woff2') format('woff2'),
        url('./assets/fonts/Poppins-Medium.woff') format('woff');
    font-weight: 500;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-SemiBold.woff2') format('woff2'),
        url('./assets/fonts/Poppins-SemiBold.woff') format('woff');
    font-weight: 600;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-BlackItalic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-BlackItalic.woff') format('woff');
    font-weight: 900;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-ExtraLightItalic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-ExtraLightItalic.woff') format('woff');
    font-weight: 200;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-BoldItalic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-BoldItalic.woff') format('woff');
    font-weight: bold;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-Light.woff2') format('woff2'),
        url('./assets/fonts/Poppins-Light.woff') format('woff');
    font-weight: 300;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-Thin.woff2') format('woff2'),
        url('./assets/fonts/Poppins-Thin.woff') format('woff');
    font-weight: 100;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-Bold.woff2') format('woff2'),
        url('./assets/fonts/Poppins-Bold.woff') format('woff');
    font-weight: bold;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Poppins';
    src: url('./assets/fonts/Poppins-Italic.woff2') format('woff2'),
        url('./assets/fonts/Poppins-Italic.woff') format('woff');
    font-weight: normal;
    font-style: italic;
}

@font-face {
    font-display: fallback;
    font-family: 'Paytone One';
    src: url('./assets/fonts/PaytoneOne-Regular.woff2') format('woff2'),
        url('./assets/fonts/PaytoneOne-Regular.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-display: fallback;
    font-family: 'Coolvetica';
    src: url('./assets/fonts/coolvetica-rg.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
}

.page-subtitle {
  font-family: 'Poppins';
  font-size: 1em;
}
.page-subtitleB {
  font-family: 'Poppins';
  font-size: 1.5em;
  font-weight: bold;
}
</style>
