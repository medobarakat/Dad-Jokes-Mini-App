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
    <h3 class="topy">{{ joke.joke }}</h3>
    <hr />
    <small class="smally">Joke id is {{ joke.id }}</small>
  </div>
</template>
<style>
.topy {
  margin-bottom: 1rem;
}
.smally {
  margin-top: 1rem;
}
</style>
