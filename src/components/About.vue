<template>
  <v-card
      outlined
      color="transparent"
  >
    <v-row justify="center">
      <v-col
          cols="12"
          md="7"
      >
        <v-card-text
            class="text-md-h6 black--text text-md-justify"
        >
          {{description.text}}
        </v-card-text>
      </v-col>
      <v-col
          cols="12"
          md="7"
      >
        <v-img
            :width="$vuetify.breakpoint.mdAndUp ? '40%' : '80%'"
            contain
            class="mx-auto"
            :src="description.title"
        >
        </v-img>
      </v-col>
      <v-col
          cols="12"
          md="7"
      >
        <v-card-text
            class="text-md-h6  black--text text-md-justify"

        >
          {{donation.text}}
        </v-card-text>
      </v-col>
    </v-row>
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
.comic-img-mdAndUp{
  border: 10px solid black;
}

.comic-img{
  border: 5px solid black;
}

.comic{
  width: 70%;
}

.comic-mdAndUp{
  width: 100%;
}

</style>
