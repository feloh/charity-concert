<template>
<v-card
    outlined
    color="transparent"
>
  <v-card-text>
    {{description.text}}
  </v-card-text>
    <v-img
        max-width="80%"
        contain
        class="mx-auto"
        :src="description.title"
    >
    </v-img>
  <v-card-text>
    {{donation.text}}
  </v-card-text>
  <v-card-text>
    <v-carousel
        cycle
        continuous
        hide-delimiters
        hide-delimiter-background
        :show-arrows="false"
        height="200"
    >
      <v-carousel-item
          v-for="(src,i) in donation.src"
          :key="i"
          class="d-flex align-center"

      >
        <v-img
            class="my-auto pa-5 carousel-img"
            :src="src"
            aspect-ratio="1.77"
        >
        </v-img>
      </v-carousel-item>
    </v-carousel>
  </v-card-text>
</v-card>
</template>

<script>
export default {
name: "About",
  props:{
  description:{
    type: Object,
    default: () =>{return {src:"", text: "Es ist ein Fehler aufgetreten."}}
  },
    donation:{
      type: Object,
      default: () => {return  {src:"", text: "Es ist ein Fehler aufgetreten."}}
    },
  }
}
</script>

<style scoped>
.carousel-img{
  border: 10px solid black;
}
</style>
