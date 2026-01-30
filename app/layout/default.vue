<template>
  <div class="min-h-screen flex flex-col bg-gray-50 text-gray-900">
    <header class="bg-slate-800 text-white shadow-md">
      <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
        <div class="flex items-center gap-2">
          <Icon name="mdi:tools" class="text-3xl text-orange-500" />
          <span class="text-2xl font-black tracking-tighter uppercase">Ferretería <span class="text-orange-500">Josu</span></span>
        </div>
        <div class="hidden md:flex gap-8 font-medium">
          <a href="#" class="hover:text-orange-400 transition">Herramientas</a>
          <a href="#" class="hover:text-orange-400 transition">Fontanería</a>
          <a href="#" class="hover:text-orange-400 transition">Electricidad</a>
        </div>
        <div class="flex items-center gap-4">
          <button class="relative p-2 hover:bg-slate-700 rounded-full transition">
            <Icon name="mdi:cart-outline" class="text-2xl" />
            <span class="absolute top-0 right-0 bg-orange-600 text-white text-[10px] font-bold px-1.5 rounded-full">0</span>
          </button>
        </div>
      </nav>
    </header>

    <main class="flex-grow container mx-auto px-6 py-10">
      <slot />
    </main>

    <footer class="bg-slate-900 text-gray-400 py-8">
      <div class="container mx-auto px-6 text-center">
        <p>&copy; 2026 Ferretería Josu - Construyendo código con Bemo.</p>
      </div>
    </footer>
  </div>
</template>