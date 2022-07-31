
<template>
 <h1> Home</h1>
 <p>{{message}}</p>
 <p>
    <button @click="decrement">+</button>
    {{number}}
    <button @click="increment">+</button>
 </p>
</template>

<script setup>
import { ref } from 'vue'
import Layout from '../Shared/Layout.vue'

const message = "Hello i am kent Jai";

const number = ref(0)

function increment(){
    number.value++;
}
function decrement(){
    number.value--;
}

</script>

<script>
export default {
    layout: Layout
}
</script>
