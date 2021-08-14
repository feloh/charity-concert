<template>
  <v-row justify="center" justify-md="start" class="px-7">
    <v-col
        style="color: white"
        cols="12"
        md="3"
        class="d-flex justify-center align-center"
        v-for="(participant,i) in participants"
        :key="i"
    >
      <v-hover
          v-slot="{ hover }"
      >
          <v-img
              aspect-ratio="1"
              :src="participant.src"
              :contain="participant.contain"
              height="100%"
          >
            <v-expand-transition>
              <div
                  v-if="$vuetify.breakpoint.mdAndUp ? hover : true"
                  class="d-flex transition-fast-in-fast-out black v-card--reveal darken-2 white--text"
              >
                <v-row>
                  <p
                      class="d-flex align-center text-center source-sans-pro pa-4"
                  >
                    {{ participant.text }}
                  </p>
                  <v-btn
                      color="red"
                      class="mx-auto source-sans-pro"
                      :href="participant.url"
                      target="_blank"
                  >
                    Besuchen
                  </v-btn>
                </v-row>
              </div>
            </v-expand-transition>
          </v-img>
      </v-hover>
    </v-col>
    <v-col
        style="color: transparent"
        cols="12"
        md="3"
        class="d-flex justify-center align-center"
        :key="i"
    >
      <v-hover
          v-slot="{ hover }"
      >
        <v-img
            aspect-ratio="1"
            :src="require('@/assets/aahr_logo.jpg')"
            contain
            height="100%"
        >
          <v-expand-transition>
            <div
                v-if="$vuetify.breakpoint.mdAndUp ? hover : true"
                class="d-flex transition-fast-in-fast-out black v-card--reveal darken-2 white--text"
            >
              <v-row justify="center">
                <p
                    class="align-center text-center source-sans-pro pa-4"
                >
                  Spende 500€ und erscheine mit deinem Unternehmen auch auf dieser Seite!
                </p>
                <v-btn
                    color="red"
                    class="mx-auto source-sans-pro"
                    href="mailto:spielmann@fraeulein-hirsch.de"
                >
                  EMAIL
                </v-btn>
              </v-row>
            </div>
          </v-expand-transition>
        </v-img>
      </v-hover>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "Participant",
  props: {
    participants:{
      type: [],
      default: () => []
    }
  }
}
</script>

<style scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .8;
  height: 100%;
}
</style>
