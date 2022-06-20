<template>
     <v-container fluid id="features" class="mt-15">
      <v-row align="center" justify="center" no-gutters>
        <v-col cols="12">
          <v-row align="center" justify="space-around" no-gutters>
            
            <v-col
              cols="12"
              sm="4"
              md="3"
              class="text-center"
              v-for="(feature, i) in features"
              :key="i"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card
                 :color="feature.color"
                  class="card"
                  tile
                  flat
                  :elevation="hover ? 10 : 4"
                  :class="{ up: hover }"
                >
                  <v-img
                    :src="feature.img"
                    max-width="200px"
                    class="d-block ml-auto mr-auto"
                    :class="{ 'zoom-efect': hover }"
                  ></v-img>
                  <h1 class="font-weight-regular mt-1">{{ feature.title }}</h1>
                  
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
          img: '/android.png',
          title: "Apps Android",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
        },
        {
          img: '/apple.png',
          title: "Apps IOS",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
        
        },
        {
          img: '/python.png',
          title: "Python",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
         
        },
         {
          img: '/vue.png',
          title: "Vue Js",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
        },
        {
          img: '/postgresql.png',
          title: "Data Base",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
        },
        {
          img: '/anaconda.png',
          title: "Data Science",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
        },
        {
          img: '/backend.png',
          title: "Backend",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
        },
        {
          img: '/rails.png',
          title: "Ecommerce",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
          color: '#f2f2f2',
        },
      ],
    }
  }
}
</script>


</script>
