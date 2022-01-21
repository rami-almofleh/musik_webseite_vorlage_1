<template>
  <q-page class="ueberuns-page">
    <section class="text-white">
      <h4 class="text-uppercase text-secondary text-bold">Über uns</h4>

      <div class="text-uppercase text-white text-bold ueberuns-text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        <br><br>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, consectetur adipiscing elit, consectetur adipiscing elit.
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </div>

    </section>
  </q-page>
</template>

<style lang="sass" scoped>
  .ueberuns-text
    @media (min-width: 768px)
      max-width: 80%
</style>

<script>
export default {
  name: 'UeberUnsPage'
}
</script>
