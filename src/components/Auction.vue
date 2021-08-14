<template>
  <div>
  <v-card
      outlined
      color="transparent"
      class="mb-15"
  >
    <v-row
        justify="center"
        class="px-7 px-md-0"
    >
      <v-col
          md="6"
          class="d-flex justify-start"
      >
        <v-img
            :src="require('@/assets/setlist.png')"
            contain
            :width="$vuetify.breakpoint.mdAndUp ? '300px' : '25px'"
        />
        <v-img
            :src="require('@/assets/auction_title.png')"
            contain
            :width="$vuetify.breakpoint.mdAndUp ? '300px' : '5px'"
        />
      </v-col>
    </v-row>
    <v-row justify-md="center" class="mt-md-15" no-gutters>
      <v-col
          cols="12"
          md="4"
      >
        <v-img
            :src="mighties.src"
            contain
            class="mx-auto"
            style="mix-blend-mode: multiply;"
        />
      </v-col>
      <v-col
          cols="12"
          md="6"
      >
      <iframe :width="$vuetify.breakpoint.mdAndUp ? '600' : '100%'" :height="$vuetify.breakpoint.mdAndUp ? '371' : '430'" seamless frameborder="0" scrolling="yes" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vS3086Tpt4swtwbVo-4Dzu7-aY9swFB9cNjMEzFd4tFOr6Gjs3q0lF-zS04GRieWOicx4zUVxEsWUgi/pubchart?oid=2040430817&amp;format=interactive"></iframe>
      </v-col>
        <v-col
          cols="12"
          md="4"
          class="d-flex flex-column align-md-center justify-md-center pa-md-10"
      >
        <v-card-text
            class="pt-8 pt-md-0 text-md-justify text-md-h6 mx-auto"
            style="max-width: 500px"
        >
          {{mighties.text}}
        </v-card-text>
        <v-card-actions>
          <v-btn
              color="#ff0000"
              class="mx-auto source-sans-pro white--text"
              elevation="8"
              href="https://docs.google.com/forms/d/e/1FAIpQLScbFnqYbzoXbavnsl8pRVV0vgnlpUrCMbDFUu7CUaLdjtkHiw/viewform?usp=sf_link"
              target="_blank"
          >
            JETZT BIETEN
          </v-btn>
        </v-card-actions>
      </v-col>
    </v-row>
  </v-card>
  <v-card
      outlined
      color="transparent"
      class="px-0 mt-15"
  >
    <v-row
        justify="center"
        class="px-7 px-md-0"
    >
      <v-col
          md="6"
          class="d-flex justify-start"
      >
        <v-img
            :src="require('@/assets/spirits.png')"
            contain
            :width="$vuetify.breakpoint.mdAndUp ? '300px' : '25px'"
        />
        <v-img
            :src="require('@/assets/auction_title.png')"
            contain
            :width="$vuetify.breakpoint.mdAndUp ? '300px' : '5px'"
        />
      </v-col>
      <v-col
          cols="12"
      >
        <v-card
            color="red"
            class="source-sans-pro white--text text-center"
        >
          Die Auktionen enden am 20.08.21 um 21:00
        </v-card>
      </v-col>
    </v-row>

    <v-card-text>
      <v-row justify="center">
        <v-col
            v-for="(spirit, i) in spirits"
            :key="`${i}-spirit`"
            cols="12"
            md="6"
        >
          <v-row no-gutters justify="center">
            <v-col
                cols="12"
                md="6"
            >
              <v-img
                  :src="require('@/assets/zoom.svg')"
                  class="py-5 d-flex align-center mx-auto"
                  height="400"
                  :width="$vuetify.breakpoint.mdAndUp ? '400' : ''"
              >
                <v-img
                    :src="spirit.src"
                    :lazy-src="require('@/assets/loading.gif')"
                    width="250"
                    class="mx-auto"
                    contain
                ></v-img>
              </v-img>
            </v-col>
            <v-col
                cols="12"
                md="6"
                class="d-flex flex-column pa-5"
            >
              <v-card-title
                  class="d-flex justify-start source-sans-pro black--text px-0"
              >
                {{spirit.title}}
              </v-card-title>
              <p class="text-md-h6 black--text">{{ spirit.text }}</p>
              <v-btn
                  color="#ff0000"
                  class="mx-auto source-sans-pro white--text"
                  elevation="8"
                  :href="spirit.url"
                  target="_blank"
              >
                JETZT BIETEN
              </v-btn>
            </v-col>
          </v-row>
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
