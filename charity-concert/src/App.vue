<template>
  <v-app>
    <v-app-bar
        app
        color="primary"
        dark
    >
      <v-img
          max-width="40%"
          class="mx-auto mt-15"
          :src="require('@/assets/logo.png')"
      ></v-img>
    </v-app-bar>
    <v-main>
      <about
          :description="description"
          :donation="donation"
      />
      <v-divider/>
      <auction
          :spirits="spirits"
          :mighties="mighties"
      />
    </v-main>
    <v-footer>
      <v-expansion-panels
          flat
      >
        <v-expansion-panel>
          <v-expansion-panel-header>
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
      src: require('@/assets/logo.png'),
      text: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.'
    },
    donation: {
      src: require('@/assets/logo.png'),
      text: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.'
    },
    spirits: [
      {
        url: 'https://monshiners.de',
        text: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et',
        src: require('@/assets/logo.png')
      },
      {
        url: 'https://simplykaschemm.de',
        text: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et',
        src: require('@/assets/logo.png')
      },
    ],
    mighties: {
      src: require('@/assets/logo.png')
    },
    imprint: {
      title: 'Impressum',
      text: 'text'
    }
  }),
};
</script>
