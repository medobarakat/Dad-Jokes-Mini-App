<script>
export default {
  name: 'AppHeader',
};
</script>
<template>
  <div class="header">
    <h1 class="title">Welcome To Dad Jokes site</h1>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/jokes">Jokes</nuxt-link>
      </li>
    </ul>
  </div>
</template>
<style>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  padding-bottom: 1rem;
  border-bottom: 1px dotted #ccc;
}
.header .title {
  font-size: 3rem;
  color: #526488;
}
ul {
  display: flex;
}
li {
  list-style: none;
}
.header a {
  display: inline-block;
  background: #ddd;
  padding: 0.3rem 1rem;
  margin-right: 0.5rem;
  color: #fff;
  text-decoration: none;
}
</style>
