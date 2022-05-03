<template>
  <section class="links-section">
      <v-container>
    <v-row>
      <v-col cols="col-4" />
      <v-col cols="col-4">
        <v-row>
          <v-col cols="col-4">
            <div>SITEMAP</div>
            <div>News</div>
            <div>How Ecosia works</div>
            <div>About us</div>
            <div>Mobile app</div>
          </v-col>
          <v-col cols="col-4">
            <div>FAQ</div>
            <div>Advertise on Ecosia</div>
            <div>Financial reports</div>
            <div>Blog</div>
            <div>Shop</div>
          </v-col>
          <v-col cols="col-4">
            <div>Imprint</div>
            <div>Ecosia GmbH</div>
            <div>12047 Berlin, Germany</div>
            <div>Chairman Christian Kroll</div>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="col-4" />
    </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {},
  mounted() {},
  unmounted() {},
  methods: {},
}
</script>

<style lang="scss" scoped>
.links-section {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 20vh;
}
</style>
