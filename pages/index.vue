<template>
    <div>
        <h1 class="text-2xl text-center">Buy BURGUEUR</h1>
        <div class="grid grid-cols-1 gap-4 p-4 md:grid-cols-2 lg:grid-cols-3">
            <DishCard v-for="burger in burgers" :key="burger.id" :burger="burger" />
        </div>
    </div>

</template>

<script setup>
import burgers from '~/data/burgers.json'

</script>