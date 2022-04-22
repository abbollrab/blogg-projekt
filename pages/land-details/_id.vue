<template>
    <div class="min-h-screen bg-coolgray">
        <div class="mx-auto w-1/2 bg-white p-5 rounded-xl">
            <h1 class="text-5xl mb-8">{{ land.title }}</h1>
            <img :src="land.image" class="w-80 h-70 border-soild border-2 border-black" />
            <p>{{ land.kontinent }}</p>
            <p>{{ land.huvudstad }}</p>
            <p class="mb-8">{{ land.population }}</p>
            <nuxt-content :document="land"></nuxt-content>
        </div>
    </div>
</template>
<script>
export default {
    async asyncData({ $content, params }) {

        let land = await $content('landposts/land' + params.id).fetch()
        console.log(land)
        return {
            land
        }
    },
}
</script>

