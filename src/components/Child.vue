<template>
    <h2>{{ name }}</h2>
    <!-- Here we are passing data as an object -->
    <h2>{{ user}}</h2>
    <h3>{{ user.email }}</h3>
    <button v-on:click="info()">Call From Parent function</button>
</template>

<script>

export default {
    name:`Child`,
    props:{
        name: String,
        user: Object,
        info:Function
    }
}
</script>