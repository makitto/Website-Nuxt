<template>
<div>
  <v-sheet color="white" height="500" class="">
    <v-row height="300" align="center" justify="center">
        <v-col cols="12">
          <v-row align="center" justify="center">
            <v-col cols="12" md="12">
              <h1 class="font-weight-normal text-h3 text-center justify-center ">Nosso Time</h1>
              <p class="align-center text-center justify-center font-weight-light text-h6 mb-3" >
              Conheça nossa equipe de desenvolvedores
              </p>
            </v-col>
          </v-row>
        </v-col>
    </v-row>
<v-container fluid id="features" class="mt-2">
    
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="space-around">
            
            <v-col
              cols="12"
              sm="3"
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
                    width="100%"
                   
                    class="d-block ml-auto mr-auto"
                    :class="{ 'zoom-efect': hover }"
                  ></v-img>
                  <h1 class="font-weight-regular">{{ feature.title }}</h1>
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
  </v-sheet>
   <v-row class="mt-10" height="300" align="center" justify="center">
        <v-col cols="12">
          <v-row align="center" justify="center">
            <v-col cols="12" md="12">
              <h1 class="font-weight-normal text-h3 text-center justify-center ">Sobre Nós</h1>
              <h1 class="align-center text-center justify-center font-weight-light text-h6 mb-3" >
               Somos uma equipe enxuta, porém dedicada e altamente comprometida com resultados. Nossos trabalhos englobam sites, aplicativos, smart contracts, softwares, games, AR/VR e mais recentemente ambientes para Metaverso.
              </h1>
            </v-col>
          </v-row>
        </v-col>
    </v-row>
    </div>
</template>

<script>
export default {
    data () {
    return {
     features: [
        {
          img: '/dev1.png',
          title: "John Doe",
          text: "Frontend Developer.",
        },
        {
          img: '/dev2.png',
          title: "Anne Maya",
          text: "Backend Developer.",
        },
        {
          img: '/dev3.png',
          title: "Joe Karl",
          text: "Full Stack Developer",
        },
         {
          img: '/dev4.png',
          title: "Karina Amber",
          text: "Data Scientist",
        },
      ],
    }
  }

}
</script>

<style>

</style>