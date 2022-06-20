<template>
  <v-carousel hide-delimiters height="600" width="100%">
    <v-carousel-item
    height="1080"
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      :to="item.to"
    >
    <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center" mt-10>
            <v-col cols="12" md="6" xl="8">
              <h1 class="display-2 font-weight-bold mb-4 mt-15" v-text="item.title"></h1>
              <h1 class="font-weight-light" v-text="item.subtitle">
                
              </h1>
              <v-btn
                rounded
                outlined
                large
                light
                @click="$vuetify.goTo('#features')"
                class="mt-5"
              >
                Saiba mais
                <v-icon class="ml-2">mdi-arrow-right</v-icon>
              </v-btn>
               </v-col>
            <v-col cols="12" md="6" xl="4" class="hidden-sm-and-down"> </v-col>
          </v-row>
        </v-col>
      </v-row>
              </v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: '/metaverse2.png',
            title:'Afinal, o que é Metaverso?',
            subtitle:'A maior revolução da era digital. Nada será como antes. Aproveite o poder da blockchain e das criptomoedas.'
          },
          {
            src: '/shop.png',
            title:'Plataformas de ecommerce',
            subtitle:'Mais de 70% das compras ocorre por meio de aplicativos. E esse número só cresce. Sua empresa vai ficar de fora?'
          },
          {
            src: '/startup.png',
            title:'Soluções para Startups',
            subtitle:'Escale seu negócio. Crie oportunidades e novos mercados. Construa aplicativos e destrave o crescimento da sua empresa.'
          },
          {
            src: '/ux.png',
            title:' UX/UI Design',
            subtitle:'Garantimps que o design projetado atenda a todas as necessidades dos usuários, e sua satisfação ao interagir com a empresa, plataformas ou marcas.'
          },
        ],
      }
    },
  }
</script>