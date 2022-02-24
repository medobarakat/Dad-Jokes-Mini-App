<script>
export default {
  name: 'joke',
  props: ['joke', 'id'],
};
</script>
<template>
  <nuxt-link :to="'/jokes/' + id">
    <div class="joke">
      <p>{{ joke }}</p>
    </div>
  </nuxt-link>
</template>
<style>
.joke {
  padding: 1rem;
  border: 1px dotted #ccc;
  margin: 1rem 0;
}
a {
  text-decoration: none;
  color: black;
  transition: all 0.4s ease-in-out;
}
a:hover {
  color: red;
}
</style>
