<template>
    <div class="bg-white rounded-b-xl pb-2 transform hover:scale-105 ease-in-out duration-500 cursor-pointer">
        <img :src="item.image" alt="land image" class="h-44 w-full object-cover" />
        <div>
            <h1 class="text-3xl pb-2 pl-2 font-serif font-medium">{{ item.title }}</h1>
            <p class="pl-2">{{ item.kontinent }}</p>
            <p class="pl-2">{{ item.huvudstad }}</p>
            <p class="pl-2">{{ item.population }}</p>
        </div>
    </div>
</template>
<script>
export default {
    props: ['item'],
    data() {
        return {
        }
    }
}
</script>
