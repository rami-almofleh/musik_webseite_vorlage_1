<template>
  <q-layout view="lHh Lpr lFf" @scroll="(e)=> scrolled = e.position">
    <q-header elevated :class="(scrolled > 20 ? '' : 'transparent')">
      <q-toolbar>
        <router-link to="/">
          <q-avatar size="4rem">
            <img src="../assets/logos/CCLogoWeiß.png" alt="">
          </q-avatar>
        </router-link>

        <q-space/>

        <q-bar class="text-white" v-if="$q.screen.gt.sm">
          <div class="q-mr-lg" @click="$router.push('/kontakt').catch(err => {})"><router-link to="/kontakt" class="kontakt-link">Kontakt</router-link></div>
          <div class="q-mr-lg" @click="$router.push('/ueberuns').catch(err => {})"><router-link to="/ueberuns" :class="$route.path.includes('ueberuns') ? 'active':''">Über uns</router-link></div>
          <div class="q-mr-lg" @click="$router.push('/team').catch(err => {})"><router-link to="/team" :class="$route.path.includes('team') ? 'active':''">Team</router-link></div>
          <div class="q-mr-lg" @click="$router.push('/beitraege').catch(err => {})"><router-link to="/beitraege" :class="$route.path.includes('beitraege') ? 'active':''">Beiträge</router-link></div>
          <div class="q-mr-lg" @click="$router.push('/videos').catch(err => {})"><router-link to="/videos" :class="$route.path.includes('videos') ? 'active':''">Videos</router-link></div>
        </q-bar>

        <q-btn
          v-if="$q.screen.lt.md"
          flat
          dense
          icon="menu"
          aria-label="Menu"
          @click="rightDrawerOpen = !rightDrawerOpen"
        />
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="rightDrawerOpen"
      side="right"
      overlay
      content-class="text-white"
    >
      <q-list class="q-pt-xl">
        <q-item clickable @click="$router.push('/videos').catch(err => {})">
          <q-item-section class="text-center text-h6">
            <router-link to="/videos">Videos</router-link>
          </q-item-section>
        </q-item>
        <q-item clickable @click="$router.push('/beitraege').catch(err => {})">
          <q-item-section class="text-center text-h6">
            <router-link to="/beitraege">Beiträge</router-link>
          </q-item-section>
        </q-item>
        <q-item clickable @click="$router.push('/team').catch(err => {})">
          <q-item-section class="text-center text-h6">
            <router-link to="/team">Team</router-link>
          </q-item-section>
        </q-item>
        <q-item clickable @click="$router.push('/ueberuns').catch(err => {})">
          <q-item-section class="text-center text-h6">
            <router-link to="/ueberuns">Über uns</router-link>
          </q-item-section>
        </q-item>
        <q-item clickable @click="$router.push('/kontakt').catch(err => {})">
          <q-item-section class="text-center text-h6">
            <router-link to="/kontakt">Kontakt</router-link>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />

      <q-footer class="absolute-bottom">
        <div class="row">
          <div class="col-xs-12 col-sm-6 col-md-6 col-lg-6 col-xl-6">
            <div class="text-h6 q-mb-md">58xxx Lüdenscheid</div>
            <div class="text-h6">Tel: xxx</div>
            <div class="text-h6">Mail: xxx</div>
          </div>

          <div :class="'col-xs-12 col-sm-6 col-md-6 col-lg-6 col-xl-6 self-center ' + ($q.screen.xs ? 'text-center q-pt-lg' : 'text-right')">
            <router-link to=""><img src="../assets/facebook.png" alt="" class="q-mr-xl"/></router-link>
            <router-link to=""><img src="../assets/instagram.png" alt="" class="q-mr-xl"/></router-link>
            <router-link to=""><img src="../assets/twitter.png" alt=""/></router-link>
          </div>
        </div>
      </q-footer>
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',

  data () {
    return {
      rightDrawerOpen: false,
      scrolled: 0
    }
  },

}
</script>
