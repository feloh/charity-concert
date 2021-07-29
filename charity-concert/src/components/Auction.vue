<template>
  <v-card>
    <v-card-title
        class="d-flex justify-center vollkorn"
    >
      Auktionen
    </v-card-title>
    <v-divider/>
    <v-card-title
        class="d-flex justify-center vollkorn"
    >
      <v-icon class="mr-1">
        mdi-music
      </v-icon>
      Setliste
    </v-card-title>
    <v-img
        :src="mighties.src"
        contain
        width="300"
        class="mx-auto"
    />
    <v-card-text>
      Einbettung
      Link zu Google Form
    </v-card-text>
    <v-card-title
        class="d-flex justify-center vollkorn"
    >
      <v-icon class="mr-1">
        mdi-glass-tulip
      </v-icon>
      Spirituosen
    </v-card-title>
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
              width="250"
              class="py-5 mx-auto"
              contain
          >
          </v-img>
        </v-col>
        <v-col
            cols="12"
            class="d-flex flex-column"
        >
          <header
              class="d-flex justify-center vollkorn"
          >
            {{spirit.title}}
          </header>
          <p>{{ spirit.text }}}</p>
          <v-btn
              class="mx-auto vollkorn"
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
