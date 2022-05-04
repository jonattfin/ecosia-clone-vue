<template>
  <v-app dark>
    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

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
  }),
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
