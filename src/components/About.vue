<template>
<v-card>
  <v-img
      max-width="70%"
      class="mx-auto"
      :src="description.src"
  ></v-img>
  <v-card-text>
    {{description.text}}
  </v-card-text>
  <v-card-title
      class="d-flex justify-center vollkorn"
  >
    Wofür sammeln wir?
  </v-card-title>
  <v-card-text>
    {{donation.text}}
  </v-card-text>
  <v-img
      max-width="70%"
      class="mx-auto"
      :src="donation.src"
  ></v-img>
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

</style>
