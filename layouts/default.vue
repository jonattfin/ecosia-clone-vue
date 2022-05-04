<template>
  <v-app dark>
    <v-app-bar dark>
      <v-menu>
        <template v-slot:activator="{ on, attrs }">
          <v-btn dark icon v-bind="attrs" v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list nav dense on>
          <v-list-item-group v-model="selectedItem" color="primary">
            <v-list-item
              v-for="(item, i) in items"
              :key="i"
              @click="navigate(item.url)"
            >
              <v-list-item-icon>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-menu>

      <v-toolbar-title>Ecosia</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <v-container fluid>
        <Nuxt />
      </v-container>
    </v-main>
    <Links />
    <v-footer>
      <v-container fluid>
        <section class="footer-section">
          Ecosia GmbH does not assume responsibility for the content of sites to
          which it links and the way in which search results are displayed.
          <br />
          To learn more please read our privacy policy and our terms of service.
        </section>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data: () => ({
    drawer: false,
    group: null,
    selectedItem: 0,
    items: [
      { text: 'Home', icon: 'mdi-folder', url: '' },
      { text: 'About us', icon: 'mdi-star', url: 'about-us' },
      // {
      //   text: 'How Ecosia works',
      //   icon: 'mdi-account-multiple',
      //   url: 'how-it-works',
      // },
      // { text: 'Mobile', icon: 'mdi-history', url: 'mobile' },
      // { text: 'Privacy', icon: 'mdi-check-circle', url: 'privacy' },
    ],
  }),
  methods: {
    navigate(url) {
      this.$router.push(`/${url}`)
    },
  },
}
</script>

<style lang="scss" scoped>
.footer-section {
  display: flex;
  height: 5vh;
  justify-content: center;
  align-items: center;

  text-align: center;
}
</style>
