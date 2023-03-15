<script setup>
    import cars from "../data/cars.json"
    import { useRouter } from "vue-router";

    const router = useRouter()

</script>
<template>
    <div>
        <div class="cars" >
            <div 
            v-for="car in cars" 
            :key="car.id"
            @click="router.push(`/cars/${car.id}`)"
            >{{ car.name }}</div>
        </div>
    </div>
</template>

<style scoped>
    .cars{
        display: flex;
    }
    .cars div{
        text-decoration: none;
        color: black;
        width: 100%;
        margin: 10px;
    }
</style>