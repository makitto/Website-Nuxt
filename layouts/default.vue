<template>
  <v-app dark>
  <v-navigation-drawer
     v-model="drawer"
      absolute
      bottom
      temporary
      app

      
  
  
      
    >
    <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <img src="/vue.png" alt="Logo" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">Agencia</v-list-item-title>
            <v-list-item-subtitle>Digital</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider />
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
       <v-layout column align-center>
               <v-flex class="mt-5"> 
                   <v-btn
                rounded
                outlined
                large
                light
                @click="$vuetify.goTo('#features')"
                class="mt-5"
              >
               Login
                <v-icon class="ml-2">mdi-login</v-icon>
              </v-btn>
                    <p class="black--text subheading mt-1 text-center">Inscreva-se</p>
               </v-flex>
               <v-flex class="mt-4 mb-4">
                <Popup />
               </v-flex>
          </v-layout>
    </v-navigation-drawer>
    <v-app-bar
      
      fixed
      app
      color="white"
      flat
    >
      <v-icon size="40" @click.stop="drawer = !drawer" >mdi-menu</v-icon>
     
      <v-toolbar-title v-text="title" />
      <v-spacer />
   
   
  <v-btn text @click="$vuetify.goTo('#hero')">
          <span class="mr-2">Home</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#features')">
          <span class="mr-2">Sobre</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#download')">
          <span class="mr-2">Portfolio</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#pricing')">
          <span class="mr-2">Vagas</span>
        </v-btn>
        <v-btn rounded outlined text @click="$vuetify.goTo('#contact')">
          <span class="mr-2">Contate-nos</span>
        </v-btn>
      
   
     <v-spacer/>
     <v-avatar size="40"  color="indigo"><v-icon color="white" large>mdi-account</v-icon>

     </v-avatar>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
   
    
    <v-footer
      :absolute="!fixed"
      app
      color="white"
      height="auto"
    >
     <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="space-around" >
            
            <v-col
              cols="12"
              sm="4"
              class="text-center"
              v-for="(feature, i) in features"
              :key="i"
            >
       
                <v-card
                  class="card"
                 tile
                 flat
                 color="white"
                 mt-15
                
                >
                  
                  <h1 class="font-weight-black secondary--text mt-15">{{ feature.title }}</h1>
                  <h4 class="font-weight-regular secondary--text subtitle-1 mt-5">
                    {{ feature.text }}
                  </h4>
                </v-card>
         
            </v-col>
          </v-row>
        </v-col>
      </v-row>

    <v-card width="100%" flat tile class="secondary black--text text-center">
      <v-card-text width="100%">
        <v-btn
          v-for="(social, i) in socials"
          :key="i"
          class="mx-4 white--text"
          :href="social.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ social.text }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
     Siga as nossas redes sociais
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong class="white--text">Nomade Digital</strong>
      </v-card-text>
    </v-card>
    
    
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      features: [
        {
          img: (""),
          title: "Onde estamos",
          text: "Somos uma empresa online. Nossa equipe está espalhada por todo o mundo",
        },
        {
          img: (""),
          title: "Fale conosco",
          text: "Mande-nos um email para xxxx@xxxx.com. Ou ligue para gente no número 55 21 xxxxxxxxxx",
        },
        {
          img: (""),
          title: "Vagas",
          text: "Quer entrar pro nosso time de desenvolvedores? Envie seu portfólio pra gente.",
        },
      ],
    socials: [
      {
        text: "mdi-facebook",
        link: "",
      },
      {
        text: "mdi-twitter",
        link: "",
      },
      {
        text: "mdi-linkedin",
        link: "",
      },
      {
        text: "mdi-instagram",
        link: "https://instagram.com/nomadedigital.io/",
      },
    ],
      
      items: [
        {
          icon: 'mdi-home',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-account-box',
          title: 'Sobre',
          to: '/sobre'
        },
        {
          icon: 'mdi-briefcase',
          title: 'Portfólio',
          to: '/portfolio'
        },
          {
          icon: 'mdi-whatsapp',
          title: 'Contato',
          to: '/portfolio'
        },
      ],
      
      miniVariant: false,
      right: false,
      left:true,
      rightDrawer: false,
      title: ''
    }
  }
}
</script>
