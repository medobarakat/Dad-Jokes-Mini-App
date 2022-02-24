<script>
import axios from 'axios';
export default {
  data() {
    return {
      joke: {},
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json',
      },
    };
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data;
      console.log(res.data.joke);
    } catch (err) {
      console.log(err);
    }
  },
};
</script>
<template>
  <div>
    <nuxt-link to="/jokes" class="btn">Back</nuxt-link>
    <h3 class="topy">{{ joke.joke }}</h3>
    <hr />
    <small class="smally">Joke id is {{ joke.id }}</small>
  </div>
</template>
<style>
.topy {
  margin: 1rem 0rem;
}
.smally {
  margin-top: 1rem;
}
.btn {
  display: inline-block;
  background: #ddd;
  padding: 0.3rem 1rem;
  margin-right: 0.5rem;
  color: #fff;
  text-decoration: none;
}
.btn:hover {
  color: cyan;
}
</style>
