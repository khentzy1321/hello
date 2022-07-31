
<template>
    <h1>My Musics</h1>
    <hr>
<div class="d-flex align-contents-between">
    <div class="card mb-3" v-for="music in musics" :key="music.id">
        <div class="card-header bg-primary">
            <h4>{{music.singer_name}}</h4>
        </div>
        <div class="card-body">
            <h5>{{music.age}}</h5>
            <h5>{{music.followers}}</h5>
            <h3>{{music.yr_release}}</h3>
            <h5>{{music.songs}}</h5>

        </div>
    </div>
</div>
</template>
<script setup>
import Layout from '../Shared/Layout.vue'
</script>

<script>
export default {
    layout: Layout,
    props: {
        musics: Array
    }
}
</script>

<style scoped>
.card {
    width: 375%;
}
</style>
