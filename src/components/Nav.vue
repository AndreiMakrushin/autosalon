<script setup>
    import {RouterLink} from "vue-router"
</script>
<template>
    <div>
        <RouterLink active-class="active" class="text" to="/">Home</RouterLink>
        <RouterLink active-class="active" class="text" to="/about">About</RouterLink>
    </div>
</template>
<style scoped>
    .active{
        font-weight: 900;
        color: orange;
        transition: .3s;
    }
    .text{
        text-decoration: none;
        font-size: 40px;
    }
</style>