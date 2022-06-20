<template>
     <v-container fluid id="features" class="mt-2">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="space-around">
            
            <v-col
              cols="12"
              sm="4"
              class="text-center"
              v-for="(feature, i) in features"
              :key="i"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card
          
                  class="card"
                 tile
                  :elevation="hover ? 10 : 4"
                  :class="{ up: hover }"
                >
        
                  <v-img
                    :src="feature.img"
                    max-width="100px"
                    class="d-block ml-auto mr-auto"
                    :class="{ 'zoom-efect': hover }"
                  ></v-img>
                  <h2 class="font-weight-regular">{{ feature.title }}</h2>
                  <h4 class="font-weight-regular subtitle-1">
                    {{ feature.text }}
                  </h4>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
</template>
<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
     
     features: [
        {
          img: require("@/static/code.png"),
          title: "Programação",
          text: "Criamos software e aplicações web e mobile para todas as plataformas.",
        },
        {
          img: '/seo.png',
          title: "Google Analitycs",
          text: " Análise de dados, big data e Data Science. Dados, dados e mais dados",
        },
        {
          img: '/commerce.png',
          title: "e-commerce",
          text: "Crie sua loja on line. Crescimento e escalabilidade para você.",
        },
      ],
    }
  }
}
</script>


</script>
