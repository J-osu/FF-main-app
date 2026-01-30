<template>
  <div class="max-w-sm rounded overflow-hidden shadow-lg bg-white border border-gray-200 hover:border-orange-500 transition-colors duration-300">
    <img class="w-full h-48 object-contain p-4" :src="product.image" :alt="product.name">
    
    <div class="px-6 py-4">
      <span class="inline-block bg-gray-100 text-gray-700 text-xs px-2 py-1 rounded-full uppercase font-bold tracking-wide">
        {{ product.brand }}
      </span>
      <div class="font-bold text-xl mb-2 text-gray-800">{{ product.name }}</div>
      <p class="text-gray-600 text-base">
        {{ product.description }}
      </p>
    </div>
    
    <div class="px-6 pt-4 pb-2 flex justify-between items-center">
      <span class="text-2xl font-bold text-orange-600">{{ product.price }}€</span>
      <button 
        @click="$emit('add-to-cart', product)"
        class="bg-orange-500 hover:bg-orange-600 text-white font-bold py-2 px-4 rounded flex items-center gap-2 transition-all"
      >
        <Icon name="mdi:cart-plus" />
        Añadir
      </button>
    </div>
  </div>
</template>

<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})

defineEmits(['add-to-cart'])
</script>