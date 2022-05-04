<template>
  <section class="links-section">
    <v-row>
      <v-col cols="col-4" />
      <v-col cols="col-4">
        <v-row class="links-container">
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
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.links-section {
  .links-container {
    display: flex;
    height: 20vh;
    justify-content: center;
    align-items: center;
  }
}
</style>
