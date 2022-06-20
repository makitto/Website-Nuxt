<template>
  <v-card id="about" class="mt-15" height="500" flat>
    <v-container fluid >
      <v-row height="500" align="center" justify="center">
        <v-col cols="12">
          <v-row align="center" justify="center">
            <v-col cols="12" md="12">
           
              <h1 class="font-weight-light display-2 text-center justify-center ">Skills</h1>
              <h1 class="align-center text-center justify-center font-weight-light text-h6 mb-3" >
                Conheça nossas competências
              </h1>
            </v-col>
          </v-row>
              <v-row>
                <v-col cols="12" md="6" class="d-flex align-center">
            <h1 class="text-h6"> Qualidade </h1><v-spacer/>
                   
               <v-rating
      v-model="rating"
      background-color="purple lighten-3"
      color="purple"
      large
    ></v-rating>
  
                </v-col>
                <v-col cols="12" md="6" class="d-flex align-center">
          <h1 class="text-h6"> Metodologia ágil </h1><v-spacer/>
                   <v-rating
      v-model="rating"
      background-color="blue"
      color="purple"
      large
    ></v-rating>
                </v-col>
                <v-col cols="12" md="6" class="d-flex align-center mt-15">
                <h1 class="text-h6"> Entrega contínua </h1> <v-spacer/>
                  <v-rating
      v-model="rating"
      background-color="purple lighten-3"
      color="red"
      large
    ></v-rating>
                </v-col>
                 <v-col cols="12" md="6" class="d-flex align-center mt-15">
                  <h1 class="text-h6"> Segurança </h1> <v-spacer/>
                   <v-rating
      v-model="rating"
      background-color="purple lighten-3"
      color="blue"
      large
    ></v-rating>
                </v-col>
              </v-row>
            </v-col>
            
          </v-row>
      
    </v-container>
  </v-card>
</template>
<script>
  export default {
    data: () => ({
      rating: 5,
    }),
  }
</script>
<style scoped>
#about {
  background-color:white
}
</style>