<template>
  <div class="container1">
    <AppHeader />
    <Nuxt />
    <AppFooter />
  </div>
</template>
<script>
import AppHeader from '../components/AppHeader.vue';
import AppFooter from '../components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppFooter,
  },
};
</script>
<style>
.container1 {
  max-width: 1200px;
  padding: 0rem 5rem;
  margin: auto;
  margin-top: 5rem;
}
</style>
