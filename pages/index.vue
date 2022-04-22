<template>
  
    <div>
      <div class="hero-image h-1/2"></div>
      <div class="flex flex-wrap justify-center">
        <div @click="goToLand(land.id)" class="w-80 m-4" v-for="land in landposts" :key="land.id">
          <landlist :item="land"></landlist>
        </div>
      </div>
    </div>
  
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData({ $content }) {
    let landposts = await $content('landposts').sortBy("id", "asc").without(['body']).fetch()
    return {
      landposts
    }
  },
  methods: {
    goToLand(id) {
      this.$router.push('/land-details/' + id)
    }
  }
}
</script>

<style>
.hero-image {
  background-image: url("https://happywall-img-gallery.imgix.net/30361/world_map_in_bright_colours_display.jpg"); /* The image used */
  height: 100px;
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
}
</style>