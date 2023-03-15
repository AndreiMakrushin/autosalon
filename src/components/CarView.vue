<script setup>
    import {useRoute, RouterView, useRouter} from "vue-router"
    import cars from "../data/cars.json"
    import ContactView from "./ContactView.vue";

    const route = useRoute()
    const router = useRouter()
    const car = cars.find(c => c.id === parseInt(route.params.id))
     
</script>
<template>
    <div>
        <h1>Название: {{ car.name }}</h1>
        <h3>Стоимость: {{ car.price }}</h3>
        <h3>Год выпуска: {{ car.year }}</h3>
        <button @click="router.push(`/cars/${car.id}/contact`)">Показать номер продавца</button>
        <RouterView />
    </div>
</template>