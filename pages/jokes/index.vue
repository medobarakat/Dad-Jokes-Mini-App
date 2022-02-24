<script>
import axios from 'axios';
import Joke from '../../components/Joke';
export default {
  data() {
    return {
      jokes: [],
    };
  },
  components: {
    Joke,
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json',
      },
    };
    try {
      const res = await axios.get('https://icanhazdadjoke.com/search', config);
      this.jokes = res.data.results;
      console.log(res.data);
    } catch (err) {
      console.log(err);
    }
  },
  head: {
    title: 'Jokes page',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Jokes page description',
      },
    ],
  },
};
</script>

<template>
  <div>
    <Joke
      v-for="joke in jokes"
      :key="joke.id"
      :joke="joke.joke"
      :id="joke.id"
    />
  </div>
</template>
