<template>
  <div class="home">
    <Banner />
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'IndexPage',
  data () {
    return {
      movies: []
    }
  },
  async fetch() {
    await this.getMovies()
  },
  methods: {
    async getMovies () {
      const data = axios.get(
        `https://api.themoviedb.org/3/movie/now_playing?api_key=${process.env.API_KEY_V3}&language=en-US&page=1`
      )

      const result = await data

      result.data.results.forEach((movie) => {
        this.movies.push(movie)
      })
    }
  }

}
</script>
