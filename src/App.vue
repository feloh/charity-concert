<template>
  <v-app>
<!--    <v-app-bar
        app
        color="#2b4d47"
        dark
    >
      <v-img
          max-width="40%"
          class="mx-auto mt-15"
          :src="require('@/assets/logo.png')"
      ></v-img>
    </v-app-bar>-->
    <v-main
        class="application"
    >
      <v-img
          max-width="90%"
          class="mx-auto"
          :src="description.src"
      ></v-img>
      <about
          :description="description"
          :donation="donation"
      />
      <auction
          :spirits="spirits"
          :mighties="mighties"
      />
    </v-main>
    <v-footer color="#ffff00">
      <v-expansion-panels
          class="application"
          flat
      >
        <v-expansion-panel>
          <v-expansion-panel-header
              class="source-sans-pro"
          >
            {{imprint.title}}
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            {{imprint.text}}
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-footer>
  </v-app>
</template>

<script>
import About from '@/components/About'
import Auction from '@/components/Auction'

export default {
  name: 'App',
  components: {
    About,
    Auction
  },
  data: () => ({
    description: {
      src: require('@/assets/aahr_logo.jpg'),
      title: require('@/assets/description_title.png'),
      text: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.'
    },
    donation: {
      src: [
        require('@/assets/dernau_test.jpg'),
        require('@/assets/dernau_test.jpg')
      ],
      text: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.'
    },
    spirits: [
      {
        url: 'https://monshiners.de',
        title: 'MONSHINERS\' OBSTBRAND 20',
        text: 'Heiß begehrt und nach 21 Minuten ausverkauft: Das war die erste Abfüllung der Monshiners aus 2020! Jetzt werden die letzten Flaschen für den guten Zweck versteigert. Das Besondere: Die Seriennummer wurden durch 40789 und 4019 ersetzt.',
        src: require('@/assets/monshiners_bottle.png')
      },
      {
        url: 'https://simplykaschemm.de',
        title: 'DON PAPA SHERRY CASK',
        text: 'Simply Kaschemm versteigert einen besonders feinen Tropfen. Der Don Papa Sherry Cask reift zunächst für vier Jahre in Ex-Bourbonfässern aus amerikanischer Weißeiche (quercus alba) und erhält anschließend für 18 Monate ein Finish in vier verschiedenen spanischen Sherryfässern (Fino, Pedro Ximenez, Cream und Palo Cortado). Auch hier wieder eine limitierte Edition.',
        src: require('@/assets/don_papa.png')
      },
    ],
    mighties: {
      src: require('@/assets/mighties_logo.jpg'),
      text: 'Die Mighties beehren uns und werden nicht irgendwelche Songs spielen. Aus 25 Songs könnt ihr die TOP 8 des Abends ersteigern. Umso mehr Geld für einen Song zusammenkommt, umso höher ist die Wahrscheinlichkeit, dass er gespielt wird!'
    },
    bands:[],
    imprint: {
      title: 'Impressum',
      text: 'text'
    }
  }),
};
</script>

<style lang="scss">
@import 'src/styles/variables.scss';

.source-sans-pro {
  font-family: Source Sans Pro, sans-serif;
  letter-spacing: 0.1em;
  font-weight: 900;
}

.application {
  background-color: #ffff00;
}
</style>
