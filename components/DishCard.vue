<template>
    <div class="bg-white shadow-lg rounded-lg">
        <img :src="burger.img" :alt="burger.name" class="rounded-t-lg">
        <div class="p-4">
            <h2 class="text-xl font-bold">{{ burger.name }}</h2>
            <p class="text-gray-500">{{ burger.description }}</p>
            <div class="flex justify-between items-center mt-4">
                <span class="font-bold text-xl">${{ burger.price }}</span>
                <button class="px-4 py-2 bg-blue-500 text-white rounded-lg" @click="addToCart(burger)">Add to
                    cart</button>
            </div>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(['burger'])

const cart = useState('cart', () => [])

function addToCart() {
    cart.value.push(props.burger)
}

</script>