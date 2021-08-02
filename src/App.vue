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
      :width="$vuetify.breakpoint.mdAndUp ? '50%' : '90%'"
      class="mx-auto mb-15"
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
        Impressum
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <h1>Impressum</h1>

        <h2>Angaben gem&auml;&szlig; &sect; 5 TMG</h2>
        <p>Felix Lohmann<br />
          Freiheit 2<br />
          40789 Monheim</p>

        <h2>Kontakt</h2>
        <p>Telefon: &#91;Telefonnummer&#93;<br />
          E-Mail: feloh@gmx.de</p>

        <p>Quelle: <a href="https://www.e-recht24.de">https://www.e-recht24.de</a></p>
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
      text: 'Am 20.08.21 wird in der Monheimer Altstadt gemeinsam für den guten Zweck gefeiert. Alle Erlöse gehen nach Dernau an die Ahr. Wie kann man helfen? Komm einfach vorbei, genieß handgemachte Live-Musik auf der großen Altstadtbühne, kalte Getränke frisch vom Fass sowie leckere Snacks und tu dabei gleichzeitig Gutes.'
    },
    donation: {
      src: [
        require('@/assets/dernau_test.jpg'),
        require('@/assets/dernau_test.jpg')
      ],
      text: 'Dernau - ein ehemals malerisches Örtchen westlich von Bad Neuenahr-Ahrweiler mit rund 1700 Einwohnern - war eines der beliebtesten Ausflugsziele an der Ahr. Bekannt für seine historischen Weinkeller, die großen Weinbauflächen und den berühmten Rotweinwanderweg zog es jedes Jahr zahlreiche Touristen an.  Durch die Flutkatastrophe wurden nun nicht nur Häuser, Autos und Brücken zerstört, auch private und berufliche Existenzen liegen in Trümmern. Um das Ahrtal und Dernau wieder in seiner alten Schönheit erstrahlen zu lassen wird jede Hilfe benötigt und dafür brauchen wir euch! '
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
  }),
};
</script>

<style lang="scss">
@import 'src/styles/variables.scss';

.source-sans-pro {
  font-family: Source Sans Pro, sans-serif;
  letter-spacing: 0.05em;
  font-weight: 900;
  word-break: normal;
}

.application {
  background-color: #ffff00;
}
</style>
