<template>
  <q-page class="videos-page">
    <section class="text-white">
      <h4 class="text-uppercase text-secondary text-bold">Videos</h4>

      <div class="row">
        <div class="col-xs-12 col-sm-3 col-md-3 col-lg-3 col-xl-3 q-pa-md" v-for="i in [1,2,3,4]">
          <q-card class="videos">
            <q-video src="https://www.youtube.com/embed/k3_tw44QsZQ?rel=0" />

            <q-card-section>
              <div class="text-h6">Our Changing Planet</div>
              <div class="text-subtitle2">by John Doe</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua.
            </q-card-section>
          </q-card>
        </div>
      </div>


    </section>
  </q-page>
</template>

<style lang="sass" scoped>
  .videos
    background-image: linear-gradient(to top, #2b0f48, #000)
</style>


<script>
export default {
  name: 'VideosPage'
}
</script>
