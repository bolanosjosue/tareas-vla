<script lang="ts">
  import MenuItem from "$lib/components/MenuItem.svelte";

  const products = [
    { title: "🥤 Coca-Cola", description: "Refresco de cola bien frío", price: "1.50", image: "https://www.shutterstock.com/image-photo/kaunas-lithuania-june-8-2022-600nw-2165590049.jpg" },
    { title: "🍊 Jugo de Naranja", description: "Natural y refrescante, sin azúcar añadida", price: "2.00", image: "https://img.freepik.com/fotos-premium/jugo-naranja-servido-restaurante-americano_1160-1712.jpg" },
  ];
</script>

<div class="min-h-screen bg-gradient-to-r from-yellow-400 to-red-500 flex flex-col items-center justify-center px-6 py-12">
  
  <a href="/" class="absolute top-6 left-6 bg-white/30 backdrop-blur-lg text-white font-bold py-3 px-5 rounded-full shadow-lg transition-all hover:bg-white/50 hover:text-black">
    ⬅️ Regresar
  </a>

  <h1 class="text-6xl font-extrabold text-white drop-shadow-lg mb-12 text-center tracking-wide">
    🥤 Bebidas Refrescantes 🍹
  </h1>

  <div class="max-w-5xl grid grid-cols-1 sm:grid-cols-2 gap-10 w-full">
    {#each products as product}
      <div class="bg-white/90 backdrop-blur-xl rounded-3xl shadow-2xl p-6 hover:shadow-red-600/50 
                  hover:scale-105 transform transition-all duration-300 overflow-hidden group text-center relative">
        
        <div class="w-40 h-40 mx-auto bg-white rounded-full flex items-center justify-center shadow-xl mb-4 group-hover:scale-110 transition">
          <img src="{product.image}" alt="{product.title}" class="w-full h-full object-cover rounded-full">
        </div>

        <h2 class="text-3xl font-bold text-red-700 group-hover:text-red-900 transition">
          {product.title}
        </h2>

        <p class="text-lg text-gray-700 my-2">{product.description}</p>

        <div class="mt-4 bg-yellow-500 text-white text-lg font-semibold py-2 px-4 rounded-full inline-block shadow-md">
          ${product.price}
        </div>
      </div>
    {/each}
  </div>
</div>
