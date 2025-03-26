<template>
  <app-header></app-header>
    <div class="container">
      <div class="py-3">
        <comp-contact></comp-contact>
      </div>
    </div>
  <app-footer></app-footer>
</template>

<script>
import compContact from './components/contact/index.vue';

export default {
  components: {
    compContact
  }
}
</script>

<style scoped>

</style>