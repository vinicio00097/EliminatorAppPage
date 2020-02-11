<template>
  <v-container>
    <v-row>
      <v-col align-self="center" sm="12" md="6" lg="6" xl="6" cols="12">
        <div class="title font-weight-regular hola2">
        Eliminator, la aplicación que te ayudará a borrar toda la información 
        de tu celular con un simple mensaje de texto. Es muy útil si quieres borrar tu información remotamente,
        sin la necesidad de tener internet. Es tan simple como agregar números y mensajes a reconocer, activar el
        sistema y listo.
        </div>
        <v-row class="pt-5"/>
        <div class="subtitle-2">
        Disponible solo para Android.
        </div>
        <v-row class="pt-2"/>
        <div>
          <img class="os-logos" src="https://unknowntechnologies.github.io/EliminatorApp/assets/android.png"/>
        </div>
      </v-col>
      <v-col sm="12" md="6" lg="6" xl="6" cols="12">
        <div align="center">
          <div class="hola" center>
            <v-carousel 
              cycle
              show-arrows-on-hover
              >
              <v-carousel-item
                v-for="(image,i) in screens"
                :key="i"
              >
                <div align="center">
                  <img class="carousel-imgs" :src="image"/>
                </div>
              </v-carousel-item>
            </v-carousel>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row class="pb-10"></v-row>
    <v-row align="center">
      <v-col align="center">
          <v-btn outlined color="green" x-large href="https://unknowntechnologies.github.io/EliminatorApp/apk/eliminator-1.0.apk">Descargar App</v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',

  data: () => ({
    colors: [
      'primary',
      'secondary',
      'yellow darken-2',
      'red',
      'orange',
    ],
    screens:[
      "https://unknowntechnologies.github.io/EliminatorApp/assets/screen-1.png",
      "https://unknowntechnologies.github.io/EliminatorApp/assets/screen-2.png",
      "https://unknowntechnologies.github.io/EliminatorApp/assets/screen-3.png",
      "https://unknowntechnologies.github.io/EliminatorApp/assets/screen-4.png",
      "https://unknowntechnologies.github.io/EliminatorApp/assets/screen-5.png",
      "https://unknowntechnologies.github.io/EliminatorApp/assets/screen-6.png"
    ]
  }),
};
</script>
<style scoped>
.carousel-imgs {
  width: 200px;
  height: 400px;
  object-fit: cover;
}

.os-logos{
  height: 100%;
  width: 30.72px;
  object-fit: cover;
}

.hola{
  max-width: 300px;
  text-align: justify;
}
</style>
