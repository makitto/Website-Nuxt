<template>
  <v-footer 
   color="white"
    dark
    padless
    
  >
    
   
    
  
      <v-row  align="center" justify="center">
        <v-col cols="12">
          <v-row align="center" justify="center">
            <v-col cols="12" md="12">
              <h1 class="font-weight-light display-2 text-center justify-center ">Entre em Contato</h1>
              <h1 class="align-center text-center justify-center font-weight-light display-1 mb-3" >
                Lorem ipsum dolor!
              </h1>
            </v-col>
          </v-row>
        </v-col>
    </v-row>
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
       
                <v-card
                  class="card"
                 tile
                 flat
                 color="white"
                
                >
                  <v-img
                    :src="feature.img"
                    max-width="100px"
                    class="d-block ml-auto mr-auto"
                  
                  ></v-img>
                  <h1 class="font-weight-black secondary--text">{{ feature.title }}</h1>
                  <h4 class="font-weight-regular secondary--text subtitle-1">
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
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet.
        Mauris cursus commodo interdum.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Nomade Digital</strong>
      </v-card-text>
    </v-card>
  </v-footer>

  

</template>

<style scoped>
.v-card {
  width: 100%;
}
</style>

<script>
export default {
  data: () => ({
     features: [
        {
          img: (""),
          title: "Onde estamos",
          text: "Somos uma empresa online. Nossa equipe está espalhada por todo o mundo",
        },
        {
          img: (""),
          title: "Fale conosco",
          text: "Mande-nos um email para xxxx@xxxx.com ou ligue para 55 21 xxxxxxxxxx",
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
  }),
};
</script>