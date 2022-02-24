<script>
export default {
  head: {
    title: 'Home page',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Home page description',
      },
    ],
  },
};
</script>

<template>
  <div class="container">
    <div>Welcome To The Site</div>
  </div>
</template>
<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
.container {
  max-width: 800px;
  margin: 2rem auto;
  overflow: hidden;
  padding: 1rem 2rem;
  background: #fff;
}
</style>
