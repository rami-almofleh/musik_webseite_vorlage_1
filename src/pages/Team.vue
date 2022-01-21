<template>
  <q-page class="team-page">
    <section class="text-white">
      <h4 class="text-uppercase text-secondary text-bold">Unser Team</h4>

      <div class="row">
        <div class="col-xs-12 col-sm-3 col-md-3 col-lg-3 col-xl-3 q-pa-md" v-for="i in [1,2,3,4]">
          <q-card class="no-border-radius transparent text-white">
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
              <div class="absolute-bottom">
                <div class="text-h6">Rami Almofleh</div>
                <div class="text-subtitle2">DJ {{i}}</div>
              </div>
            </q-img>
          </q-card>
        </div>
      </div>
    </section>
  </q-page>
</template>

<style lang="sass" scoped>
  .q-img
    height: 20rem
</style>

<script>
export default {
  name: 'TeamPage'
}
</script>
