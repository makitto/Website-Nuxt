<template>
<div>
<Caroussel/>
<Services/>
<Banner/>
<Porfolio/>
<br/>
<About/>
<br/>
<Team/>
<br/>
<Login/>

<!--
<v-row justify="center" align="center">
          <v-col
            v-for="n in 3"
            :key="n"
            cols="4"
          >
            <v-card height="200"></v-card>
          </v-col>
        </v-row>
  <v-row justify="center" align="center">
    
    <v-col cols="12" sm="8" md="12" >
      <v-card class="logo py-4 d-flex justify-center">
        <NuxtLogo />
        <VuetifyLogo />
      </v-card>
      <v-card>
        <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title>
        <v-card-text>
          <p>Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
          <p>
            For more information on Vuetify, check out the <a
              href="https://vuetifyjs.com"
              target="_blank"
              rel="noopener noreferrer"
            >
              documentation
            </a>.
          </p>
          <p>
            If you have questions, please join the official <a
              href="https://chat.vuetifyjs.com/"
              target="_blank"
              rel="noopener noreferrer"
              title="chat"
            >
              discord
            </a>.
          </p>
          <p>
            Find a bug? Report it on the github <a
              href="https://github.com/vuetifyjs/vuetify/issues"
              target="_blank"
              rel="noopener noreferrer"
              title="contribute"
            >
              issue board
            </a>.
          </p>
          <p>Thank you for developing with Vuetify and I look forward to bringing more exciting features in the future.</p>
          <div class="text-xs-right">
            <em><small>&mdash; John Leider</small></em>
          </div>
          <hr class="my-3">
          <a
            href="https://nuxtjs.org/"
            target="_blank"
            rel="noopener noreferrer"
          >
            Nuxt Documentation
          </a>
          <br>
          <a
            href="https://github.com/nuxt/nuxt.js"
            target="_blank"
            rel="noopener noreferrer"
          >
            Nuxt GitHub
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
<v-row  justify="center" align-center no-gutters>
          <v-col
            v-for="n in 4"
            :key="n"
            cols="3"
            
          >
            <v-card height="200"></v-card>
          </v-col>
          <v-col
            v-for="n in 4"
            :key="n"
            cols="3"
            
          >
            <v-card height="200"></v-card>
          </v-col>
        </v-row>
         <v-banner two-line>
    <v-avatar
      slot="icon"
      color="deep-purple accent-4"
      size="40"
    >
      <v-icon
        icon="mdi-lock"
        color="white"
      >
        mdi-lock
      </v-icon>
    </v-avatar>

    Three line text string example with two actions. One to two lines is preferable. Three lines should be considered the maximum string length on desktop in order to keep messages short and actionable.

    <template v-slot:actions>
      <v-btn
        text
        color="deep-purple accent-4"
      >
        Action
      </v-btn>
      <v-btn
        text
        color="deep-purple accent-4"
      >
        Action
      </v-btn>
    </template>
  </v-banner>
 <v-row  justify="center" align-center no-gutters>
          <v-col
            v-for="n in 4"
            :key="n"
            cols="6"
            
          >
            <v-card height="200"><v-slider
          v-model="radius"
          label="Radius"
          min="0"
          max="25"
          thumb-label
        ></v-slider></v-card>
          </v-col>
 </v-row>
 <v-card class="mx-auto" width="100%" color="green" height="100%"  justify="center" align-center >
<v-row dense  justify="center" align-center gutters>
        
          <v-col
            v-for="n in 4"
            :key="n"
            cols="3"
            
          >
            <v-card height="300" width="auto"></v-card>
          </v-col>
        </v-row>
 </v-card>
          <v-banner two-line>
    <v-avatar
      slot="icon"
      color="deep-purple accent-4"
      size="40"
    >
      <v-icon
        icon="mdi-lock"
        color="white"
      >
        mdi-lock
      </v-icon>
    </v-avatar>

    Three line text string example with two actions. One to two lines is preferable. Three lines should be considered the maximum string length on desktop in order to keep messages short and actionable.

    <template v-slot:actions>
      <v-btn
        text
        color="deep-purple accent-4"
      >
        Action
      </v-btn>
      <v-btn
        text
        color="deep-purple accent-4"
      >
        Action
      </v-btn>
    </template>
  </v-banner>-->
 
</div>
</template>

<script>
import Porfolio from "../components/Porfolio.vue";
export default {
    name: "IndexPage",
    components: { Porfolio }
}
</script>
