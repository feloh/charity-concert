<template>
  <v-card>
    <v-card-title>Auktionen</v-card-title>
    <v-card-subtitle>Setliste</v-card-subtitle>
    <v-img
        :src="mighties.src"
        contain
    />
    <v-card-text>
      Einbettung
      Link zu Google Form
    </v-card-text>
    <v-card-subtitle>Spirituosen</v-card-subtitle>
    <v-card-text
        v-for="(spirit, i) in spirits"
        :key="`${i}-spirit`"
    >
      <v-row no-gutters>
        <v-col
            cols="12"
        >
          <v-img
              :src="spirit.src"
              contain
          >
          </v-img>
        </v-col>
        <v-col
            cols="12"
            class="d-flex flex-column"
        >
          <p>{{ spirit.text }}}</p>
          <v-btn
              class="mx-auto"
          >
            Jetzt Bieten
          </v-btn>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "Auction",
  props: {
    spirits: {
      type: Array,
      default: () => {
        return [
          {
            url: 'https://monshiners.de',
            text: 'Es ist ein Fehler aufgetreten',
            src: ''
          },
          {
            url: 'https://simply-kaschemm.com/',
            text: 'Es ist ein Fehler aufgetreten',
            src: ''
          }
        ]
      }
    },
    mighties: {
      type: Object,
      default: () =>{return {src: require('@/assets/logo.png')}}
    }
  }
}
</script>

<style scoped>

</style>
