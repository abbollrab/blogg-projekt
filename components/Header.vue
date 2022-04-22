<template>
    <div class="bg-white z-10 pb-4 sticky inset-x-0 top-0 border-soild border-2 border-coolgray">
        <h1 class="text-center text-3xl">Olles Landblogg</h1>
        <div class="text-center">
            <nuxt-link
                to="/"
                class="border-solid border border-gray-500 bg-white rounded-md mx-2 hover:bg-gray-200 focus:bg-gray-200 focus:outline-none focus:ring-2 focus:ring-gray-200 focus:ring-opacity-50"
            >Hem</nuxt-link>
            <nuxt-link
                to="about-me"
                class="border-solid border border-gray-500 rounded-md mx-2 hover:bg-gray-100 focus:bg-gray-200 focus:outline-none focus:ring-2 focus:ring-gray-200 focus:ring-opacity-50"
            >Om oss</nuxt-link>

            <a href="https://twitter.com/BarackObama" class="float-right">
                <img id="twitterbild" src="/black-and-white-twitter-logo-transparent_100736.png" class="w-8 h-8" />
            </a>
            <a href="https://www.instagram.com/barackobama/" class="float-right">
                <img id="instagrambild" src="/SocialMedia_Instagram-Outline-512.png" class="w-8 h-8"/>
            </a>
        </div>
    </div>
</template>

<style>

#twitterbild:hover{
    transform: scaleX(-1);
}
#instagrambild:hover{
    transform: scaleX(-1);
}
</style>