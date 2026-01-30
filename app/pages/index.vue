<template>
  <div>
    <section class="mb-10 text-center">
      <h1 class="text-4xl font-extrabold text-slate-800 mb-4">Herramientas de Profesional</h1>
      <p class="text-lg text-slate-600">Si no lo tenemos nosotros, es que no existe (o se ha perdido en el almacén).</p>
    </section>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
      <ProductCard 
        v-for="item in products" 
        :key="item.id" 
        :product="item" 
        @add-to-cart="handleAddToCart"
      />
    </div>
  </div>
</template>

<script setup>
const products = ref([
  {
    id: 1,
    name: 'Taladro Percutor 800W',
    brand: 'Makita-Fake',
    price: 89.95,
    description: 'Perfora hasta el hormigón más duro y la paciencia de tus vecinos.',
    image: 'https://images.unsplash.com/photo-1504148455328-c376907d081c?q=80&w=500&auto=format&fit=crop'
  },
  {
    id: 2,
    name: 'Juego de Destornilladores (12 pzs)',
    brand: 'Ironside',
    price: 24.50,
    description: 'Puntas imantadas para que no pierdas el tornillo (ni la cordura).',
    image: 'https://images.unsplash.com/photo-1530124560072-a0c97c7eb780?q=80&w=500&auto=format&fit=crop'
  },
  {
    id: 3,
    name: 'Martillo de Oreja Profesional',
    brand: 'Steel-Strong',
    price: 15.99,
    description: 'Mango ergonómico. Ideal para clavos rebeldes.',
    image: 'https://images.unsplash.com/photo-1586864387917-f539470d6bb0?q=80&w=500&auto=format&fit=crop'
  }
])

const handleAddToCart = (product) => {
  console.log(`Bemo Log: Añadiendo al carrito -> ${product.name}`)
  alert(`¡${product.name} añadido! (Aunque aún no tenemos carrito real, Josu)`)
}
</script>