<template>
  <q-page>

    <section class="header-section">
      <div class="header-section__top">
        <div class="text-h6 text-warning text-weight-light">WED 2020, 2019</div>
        <div class="bg-secondary text-h4 text-weight-light q-mb-lg">WED 2020, 2019</div>
        <div :class="'text-bold text-white text-uppercase ' + ($q.screen.xs ? 'text-h3 q-mb-md' : 'text-h2 q-mb-lg')">kill the <br>noise party</div>
        <div class="text-white text-h6 text-weight-light q-mb-lg">text</div>

        <q-btn no-caps color="primary" to="/ueberuns">Mehr über uns</q-btn>
      </div>
      <div class="header-section__bottom row">
        <div class="col-xs-12 col-sm-4 col-md-4 col-lg-4 col-xl-4 q-pa-md" v-for="i in [1,2,3]">
          <div class="header-persone q-pa-md relative-position shadow-16">
            <div class="row absolute-bottom q-pt-xl">
              <div class="text-h5 text-white q-mb-md text-bold">Anna Lee</div>
              <p class="q-mb-md text-white">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
              <q-btn color="secondary">Mehr lesen</q-btn>
            </div>

          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="row">
        <div class="col-xs-12 col-sm-4 col-md-4 col-lg-4 col-xl-4 q-pa-md" v-for="i in [1,2,3]">
          <div class="party q-pa-md relative-position shadow-16">
            <div class="absolute-bottom q-pt-xl party-text">
              <div class="text-h5 text-white q-mb-md text-bold block q-pl-none">Anna Lee</div>
              <div class="q-mb-md text-white">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </div>
            </div>

          </div>
        </div>
      </div>
    </section>

    <section class="popular-section">
      <div class="text-h4 text-uppercase text-white">popular dj</div>
      <div class="row">
        <div class="col-xs-12 col-sm-3 col-md-3 col-lg-3 col-xl-3 q-pa-md" v-for="i in [1,2,3,4]">
          <q-card class="no-border-radius transparent text-white">
            <q-img
              src="https://cdn.quasar.dev/img/parallax2.jpg"
            />
            <q-card-section class="q-pl-none">
              <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
              <div>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              </div>
            </q-card-section>
          </q-card>
        </div>
      </div>

    </section>

  </q-page>
</template>

<script>
export default {
  name: 'PageIndex'
}
</script>
