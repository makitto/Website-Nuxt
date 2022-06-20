<template>


      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
             <v-col cols="12" md="4" sm="4">
           <p class="font-weight-normal text-h3 text-center justify-center ">Cadastre-se</p>
               <p class="align-center text-center justify-center font-weight-light text-h5 mb-3" >
              E fique por dentro das novidades do mundo da tecnologia.
              </p>
          </v-col>
          <v-col cols="12" sm="8" md="8">
            <v-card class="elevation-12">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 black--text text--accent-3"
                        >Bem vindo  </h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-facebook</v-icon>
                          </v-btn>

                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-google</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-linkedin</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">Faça o seu login</h4>
                        <v-form>
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="mdi-email"
                            type="text"
                            color="blue"
                          />

                          <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            prepend-icon="mdi-lock"
                            type="password"
                            color="blue"
                          />
                        </v-form>
                        <h3 class="text-center mt-4">Esqueceu sua senha ?</h3>
                      </v-card-text>
                      <div class="text-center mt-3">
                        <v-btn rounded color="blue" dark class="text-button">LOGIN</v-btn>
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="blue">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Ainda não é cadastrado?</h1>
                        <h5
                          class="text-center"
                        >Insira seus dados e comece a jornada conosco </h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined dark @click="step++">CADASTRE-SE</v-btn>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row class="fill-height">
                    <v-col cols="12" md="4" class="blue">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Já é cadastrado?</h1>
                        <h5
                          class="text-center"
                        >Para se conectar por favor faça o login</h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined dark @click="step--">Login</v-btn>
                      </div>
                    </v-col>

                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1 class="text-center display-2 black--text text--accent-3">Crie sua Conta</h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-facebook</v-icon>
                          </v-btn>

                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-google</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-linkedin</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">Registre-se com seu e-mail</h4>
                        <v-form @submit="formSubmit">
                          <v-text-field
                            label="Nome"
                            name="Nome"
                            prepend-icon="mdi-account"
                            type="text"
                            color="teal accent-3"
                          />
                           <v-text-field
                            label="Sobrenome"
                            name="Sobrenome"
                            prepend-icon="mdi-account"
                            type="text"
                            color="teal accent-3"
                          />
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="mdi-email"
                            type="text"
                            color="blue"
                          />

                          <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            prepend-icon="mdi-lock"
                            type="password"
                            color="blue"
                          />
                        </v-form>
                      </v-card-text>
                      <div class="text-center mt-n5">
                        <v-btn  rounded color="blue" dark>SIGN UP</v-btn>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
         
        </v-row>

      </v-container>

</template>

<script>
export default {
  data: () => ({
    step: 1
  }),
  props: {
    source: String
  }
};
</script>
