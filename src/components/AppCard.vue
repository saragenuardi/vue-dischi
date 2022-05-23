<template>

    <div class="card ">
        <img :src="album.poster" :alt="album.title">
        <h3>{{ album.title}}</h3>
        <p> {{ album.author}}</p>
        <p>{{ album.year}}</p>
    </div>

</template>

<script>
export default {
    name: 'AppCard',
    props: {
        album: Object
    }
}
</script>

<style lang="scss" scoped>

</style>