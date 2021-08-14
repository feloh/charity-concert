<template>
  <v-card
      outlined
      color="transparent"
  >
    <v-row justify="center" class="mb-15">
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
      <v-col
          cols="12"
          md="7"
      >
        <v-img
            :width="$vuetify.breakpoint.mdAndUp ? '40%' : '80%'"
            contain
            class="mx-auto"
            :src="description.help"
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
          <p>
            {{donation.donation}}
          </p>
          <v-row
              class="my-5"
              justify="space-around"
          >
            <v-col
                cols="12"
                md="6"
            >
              <p
                  class=" text-center source-sans-pro red--text"
              >
                IBAN DE 51 3056 0548 0029 6900 14
              </p>
            </v-col>
          <v-col
              cols="12"
              md="6"
              class="d-flex justify-center"
          >
            <v-btn
                color="#ff0000"
                class="source-sans-pro white--text"
                elevation="8"
                target="_blank"
                href="https://paypal.me/pools/c/8BJkhuYJZc"
            >
              PAYPAL
            </v-btn>
          </v-col>
          </v-row>
          <p>
          {{donation.help}}
          </p>
          <p
              class="d-flex justify-center"
          >
            Du hast eine Idee oder willst helfen? Hier kannst du dich melden:
          </p>
          <v-row
              class="mt-5"
              justify="center"
              justify-md="space-around"
          >
            <a
                class="source-sans-pro red--text"
                href="mailto:spielmann@fraeulein-hirsch.de"
            >
              spielmann@fraeulein-hirsch.de
            </a>
            <a
                class="source-sans-pro red--text mt-10 mt-md-0"
                href="mailto:felix@monshiners.de"
            >
              felix@monshiners.de
            </a>
          </v-row>
        </v-card-text>
      </v-col>
      <v-col
          cols="12"
          md="7"
      >
        <v-img
            :width="$vuetify.breakpoint.mdAndUp ? '50%' : '80%'"
            contain
            class="mx-auto"
            :src="description.lineUp"
        >
        </v-img>
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
