<template>
  <div>
    <div ref="WA" class="elfsight-app-28b882e4-f8b5-4b5a-8994-adc90489c91a"></div>
    <v-carousel hide-delimiters :height="windowSize > 2 ? 500 : 250" continuous cycle>
      <v-carousel-item
        v-for="(photo, index) in photos"
        :key="index"
        :src="photo.src"
      >
      </v-carousel-item>
    </v-carousel>
    <v-flex xs12>
      <v-divider horizontal></v-divider>
    </v-flex>
    <!-- Brochure -->
    <div class="fade-in full-width">
      <v-layout row wrap>
        <v-flex md6 xs12 justify-center text-center align-center class=my-auto>
          <v-flex px-10 xs12>
            <span class="page-title">Diseño y Impresiónes de Boletines, Menus y Tarjetas de Presentación</span>
            <v-flex xs12 px-10>
              <v-divider horizontal></v-divider>
            </v-flex>
            <v-flex xs12 pt-10 class="page-text">
              <span>Contamos con un Equipo de Diseñadores para implementar la solucion que nececites para tu Empresa de Pequeña a Media Escala; como Boletines, Menus, Tarjetas de Presentación, Manuales, Tabloides, Boletos, y mas.. </span>
            </v-flex>
          </v-flex>
        </v-flex>
        <v-flex md6 text-center py-10 xs12>
          <img width="70%" style="border-radius: 20px;" src="../assets/training.png"/>
        </v-flex>
      </v-layout>
    </div>
    <!-- T shirt Quotes -->
    <div class="fade-in full-width">
      <v-layout row wrap style="background-color: #F6F6F6">
        <v-flex xs12>
          <v-divider horizontal></v-divider>
        </v-flex>
        <v-flex text-center xs12 pl-10 pt-10 class="page-title">
          Impresiónes a todo Color
          <v-flex xs4 class="mx-auto" pb-10>
            <v-divider horizontal></v-divider>
          </v-flex>
        </v-flex>
        <v-flex sm6 md4 lg3 xs12 text-center py-5 v-for="printtype in printTypes" :key="printtype.name">
          <v-hover v-slot:default="{ hover }">
            <v-card
              @click="generateQuoteDialog(printtype.name)"
              :elevation="hover ? 12 : 2"
              class="mx-auto"
              max-width="300"
              style="border-radius: 25px;"
            >
              <v-img class="mx-auto shirts" :src="printtype.src" width="300px">
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-slow-in-fast-out black darken-2 v-card--reveal white--text"
                    style="height: 100%; border-radius: 25px;"
                  >
                   <span class="page-subtitleB">Cotiza Gratis!</span>
                  </div>
                </v-expand-transition>
              </v-img>
            </v-card>
          </v-hover>
        </v-flex>
        <v-flex xs12 pt-10>
          <v-divider horizontal></v-divider>
        </v-flex>
      </v-layout>
    </div>
    <!-- Machines -->
    <div class="fade-in full-width">
      <v-layout row wrap pt-10>
        <v-flex md7 py-10 xs12>
          <v-img src="../assets/ourmachines.jpg">
          </v-img>
          <v-img src="../assets/ourmachines2.jpg">
          </v-img>
        </v-flex>
        <v-flex md5 xs12 text-center pa-10 class="mx-auto">
          <v-flex xs12 pt-10 class="page-title">
            Calidad y Durabilidad
            <v-divider horizontal></v-divider>
          </v-flex>
          <v-flex xs12 class="page-text" pt-10>
            Como empresa priorizamos la calidad y durabilidad de nuestros productos, por lo tanto usamos equipo Profesional para poder brindar productos de alta calidad a nuestros clientes, garantizados.
          </v-flex>
        </v-flex>
        <v-flex xs12 pt-10>
          <v-divider horizontal></v-divider>
        </v-flex>
      </v-layout>
    </div>
    <!-- Contact us -->
    <div class="fade-in full-width">
      <v-layout row wrap pt-10 style="background-color: #F6F6F6">
        <v-flex md6 xs12 px-5 py-10>
          <v-card class="mx-auto" max-width="600px">
            <v-card-title class="page-title">Buscas imprimir un Diseño?</v-card-title>
            <v-card-text>
              <v-layout row wrap pt-5>
                <v-flex xs12 px-5>
                  <v-text-field
                    label="Nombre"
                    outlined
                    prepend-inner-icon="mdi-account"
                  />
                </v-flex>
                <v-flex xs12 px-5>
                  <v-text-field
                    label="Telefono"
                    prepend-inner-icon="mdi-phone"
                    outlined
                  />
                </v-flex>
                <v-flex xs12 px-5>
                  <v-text-field
                    prepend-inner-icon="mdi-email"
                    label="Correo"
                    outlined
                  />
                </v-flex>
                <v-flex xs12 px-5>
                  <v-text-field
                    label="Describe tu Diseño"
                    prepend-inner-icon="mdi-message"
                    outlined
                    height="100px"
                  />
                </v-flex>
              </v-layout>
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn dark tile depressed class="text-capitalize" color="green" @click="shirtQuoteDialog = false">Enviar Cotizacion</v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
        <v-flex md6 xs12 text-center class="my-auto">
          <v-flex xs12 class="page-titleLG">
            Diseña
          </v-flex>
          <v-flex xs12 class="page-titleLG">
            Cotiza
          </v-flex>
          <v-flex xs12 class="page-titleLG">
            Imprime
          </v-flex>
          <v-flex pb-10 xs12 class="page-subtitle">
            IMATEQ.MX
            <v-flex xs2 class="mx-auto">
              <v-divider horizontal>
              </v-divider>
            </v-flex>
            <v-flex xs12 pt-2>
              <a style="text-decoration: none;" href="https://www.facebook.com">
                <v-icon large color="black">mdi-facebook</v-icon>
              </a>
              <a style="text-decoration: none;" href="https://www.instagram.com">
                <v-icon large color="black">mdi-instagram</v-icon>
              </a>
              <a style="text-decoration: none;"  href="https://www.whatsapp.com">
                <v-icon large color="black">mdi-whatsapp</v-icon>
              </a>
            </v-flex>
          </v-flex>
        </v-flex>
        <v-flex xs12 pt-10>
          <v-divider horizontal></v-divider>
        </v-flex>
      </v-layout>
    </div>
    <!-- Map -->
    <div>
      <v-layout text-center align-center justify-center style="background-color: white">
        <div class="mapouter">
          <div class="gmap_canvas">
            <iframe width="100%" height="500" id="gmap_canvas" src="https://maps.google.com/maps?q=Calle%2016%20de%20Septiembre%20915%2C%20Independencia%2C%2064720%20Monterrey%2C%20N.L.&t=&z=17&ie=UTF8&iwloc=&output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0">
            </iframe>
          </div>
        </div>
      </v-layout>
    </div>
    <v-dialog v-model="dialogSuccess" max-width="290" persistent>
      <v-card>
        <v-card-title class="headline">Éxito</v-card-title>
        <v-card-text>Action successful.</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn dark color="green" @click="dialogSuccess = false">Aceptar</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
    <v-dialog v-model="shirtQuoteDialog" max-width="800">
      <v-card>
        <v-card-title class="headline">Cotiza tu Impresión a {{ shirtQuoteForm.productName }}</v-card-title>
        <v-card-text>
          <v-layout row wrap pt-5>
            <v-flex xs12 px-5>
              <v-text-field
                :rules="[() => shirtQuoteForm.contactName.length > 0]"
                label="Nombre"
                outlined
                prepend-inner-icon="mdi-account"
              />
            </v-flex>
            <v-flex xs12 px-5>
              <v-text-field
                :rules="[() => shirtQuoteForm.phone.length > 0]"
                label="Telefono"
                prepend-inner-icon="mdi-phone"
                outlined
              />
            </v-flex>
            <v-flex xs12 px-5>
              <v-text-field
                :rules="[() => shirtQuoteForm.email.length > 0]"
                prepend-inner-icon="mdi-email"
                label="Correo"
                outlined
              />
            </v-flex>
            <v-flex xs12 px-5>
              <v-text-field
                :rules="[() => shirtQuoteForm.message.length > 0]"
                label="Describe tu Diseño"
                prepend-inner-icon="mdi-message"
                outlined
                height="100px"
              />
            </v-flex>
          </v-layout>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn text class="text-capitalize" color="red" @click="shirtQuoteDialog = false">Cancelar</v-btn>
          <v-btn dark tile depressed class="text-capitalize" color="green" @click="shirtQuoteDialog = false">Enviar Cotizacion</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  components: {
  },
  data: () => ({
    printTypes: [
      {
        name: 'Serigrafia',
        src: require('../assets/portfolio1.jpg')
      },
      {
        name: 'Transferencia',
        src: require('../assets/portfolio2.jpg')
      },
      {
        name: 'Vinil Textil',
        src: require('../assets/portfolio3.jpg')
      },
      {
        name: 'Sublimado',
        src: require('../assets/portfolio4.jpg')
      }
    ],
    photos: [
      {
        src: require('../assets/barniz.jpg')
      },
      {
        src: require('../assets/digital.jpg')
      },
      {
        src: require('../assets/doblez.jpg')
      },
      {
        src: require('../assets/guillotina.jpg')
      }
    ],
    dialogSuccess: false,
    fadeInElements: [],
    formIsValid: false,
    shirtQuoteDialog: false,
    shirtQuoteForm: {
      productName: '',
      contactName: '',
      email: '',
      message: '',
      phone: '',
      image: ''
    }
  }),
  methods: {
    generateQuoteDialog (product) {
      this.shirtQuoteForm.productName = product
      this.shirtQuoteDialog = true
    },
    pushAndResetNav (route) {
      if (this.$route.path !== route) {
        this.$router.push(route)
      }
    }
  },
  computed: {
    windowSize () {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs': return 0
        case 'sm': return 1
        case 'md': return 2
        case 'lg': return 3
        case 'xl': return 4
        default: return 0
      }
    }
  },
  mounted () {
    const foo = document.createElement('script')
    foo.setAttribute('src', 'https://apps.elfsight.com/p/platform.js')
    this.$refs.WA.appendChild(foo)
    var handleScroll = (evt) => {
      for (var i = 0; i < this.fadeInElements.length; i++) {
        var elem = this.fadeInElements[i]
        if (isElemVisible(elem)) {
          elem.style.opacity = '1'
          elem.style.transform = 'scale(1)'
          this.fadeInElements.splice(i, 1) // only allow it to run once
        }
      }
    }
    var isElemVisible = (el) => {
      var rect = el.getBoundingClientRect()
      var elemTop = rect.top + 200 // 200 = buffer
      var elemBottom = rect.bottom
      return elemTop < window.innerHeight && elemBottom >= 0
    }

    this.fadeInElements = Array.from(document.getElementsByClassName('fade-in'))
    document.addEventListener('scroll', handleScroll)
    handleScroll()
  },
  unmounted () {
    var handleScroll = (evt) => {
      for (var i = 0; i < this.fadeInElements.length; i++) {
        var elem = this.fadeInElements[i]
        if (isElemVisible(elem)) {
          elem.style.opacity = '1'
          elem.style.transform = 'scale(1)'
          this.fadeInElements.splice(i, 1) // only allow it to run once
        }
      }
    }
    var isElemVisible = (el) => {
      var rect = el.getBoundingClientRect()
      var elemTop = rect.top + 200 // 200 = buffer
      var elemBottom = rect.bottom
      return elemTop < window.innerHeight && elemBottom >= 0
    }
    document.removeEventListener('scroll', handleScroll)
  }
}
</script>

<style scoped>
.mapouter{
  position: relative;
  text-align:right;
  height:500px;
  width:100%;
}
.gmap_canvas {
  overflow:hidden;
  background:none!important;
  height:500px;
  width:100%;
}
.page-title {
  font-family: 'Coolvetica';
  font-size: 3em;
}
.page-titleLG {
  font-family: 'Coolvetica';
  font-size: 5em;
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
.page-text {
  font-family: 'Poppins';
  font-size: 1.5em;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
.shirts {
  border-radius: 25px;
  -webkit-filter: grayscale(100%); /* Safari 6.0 - 9.0 */
  filter: grayscale(30%);
}
.fade-in {
  opacity: 0;
  transition: 0.3s all ease-out;
  transform: scale(0.8);
  box-sizing: border-box;
  display: inline-block;
}
.full-width{
  width: 100%;
}
</style>
