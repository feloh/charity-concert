<template>
  <div>
  <v-card
      outlined
      color="transparent"
      class="px-0 mb-10"
  >
    <v-img
        :src="require('@/assets/auction_title.png')"
        contain
        max-width="90%"
        class="mx-auto"
    />
    <v-img
        :src="require('@/assets/setlist.png')"
        contain
        max-width="90%"
        class="mx-auto mt-10"    />
    <v-card-text class="pt-8">
      {{mighties.text}}
    </v-card-text>
    <v-img
        :src="mighties.src"
        contain
        width="300"
        class="mx-auto"
        style="mix-blend-mode: multiply;"
    />
    <v-card-actions>
      <v-btn
          color="#ff0000"
          class="mx-auto source-sans-pro white--text"
          elevation="8"
      >
        JETZT BIETEN
      </v-btn>
    </v-card-actions>
  </v-card>
  <v-card
      outlined
      color="transparent"
      class="px-0"
  >
    <v-img
        :src="require('@/assets/spirits.png')"
        contain
        max-width="90%"
        class="mx-auto"
    />
    <v-card-text
        v-for="(spirit, i) in spirits"
        :key="`${i}-spirit`"
    >
      <v-row no-gutters>
        <v-col
            cols="12"
        >
          <v-img
              :src="require('@/assets/zoom.svg')"
              class="py-5 d-flex align-center"
              height="400"
          >
            <v-img
                :src="spirit.src"
                width="250"
                class="mx-auto"
                contain
            ></v-img>
          </v-img>
        </v-col>
        <v-col
            cols="12"
            class="d-flex flex-column"
        >
          <v-card-title
              class="d-flex justify-start source-sans-pro black--text px-0"
          >
            {{spirit.title}}
          </v-card-title>
          <p>{{ spirit.text }}</p>
          <v-btn
              color="#ff0000"
              class="mx-auto source-sans-pro white--text"
              elevation="8"
          >
            JETZT BIETEN
          </v-btn>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
  </div>
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
      default: () =>{return {src: '', text:'Es ist ein Fehler aufgetreten'}}
    }
  }
}
</script>

<style scoped>

</style>
