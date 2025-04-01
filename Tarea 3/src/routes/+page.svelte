<script lang="ts">
	const categories = [
	  { name: "Bebidas", path: "/bebidas", image: "https://cdn-icons-png.flaticon.com/512/3075/3075975.png" }, // Vaso de bebida
	  { name: "Combos", path: "/combos", image: "https://img.freepik.com/vector-premium/combo-comida-rapida_18591-35736.jpg" }, // Combo con papas y bebida
	  { name: "Desayunos", path: "/desayunos", image: "https://cdn-icons-png.flaticon.com/512/9008/9008111.png" }, // Plato de desayuno
	  { name: "Ensaladas", path: "/ensaladas", image: "https://cdn-icons-png.flaticon.com/512/4063/4063400.png" }, // Ensalada
	  { name: "Hamburguesas", path: "/hamburguesas", image: "https://static.vecteezy.com/system/resources/previews/014/720/138/non_2x/hamburger-food-cartoon-burgers-icon-juicy-tasty-hamburger-flat-icon-illustration-isolated-on-white-background-free-vector.jpg" }, // Hamburguesa
	  { name: "Postres", path: "/postres", image: "https://cdn-icons-png.flaticon.com/512/5347/5347946.png" }, // Helado
	];
  </script>
  
  <div class="min-h-screen bg-gradient-to-b from-yellow-100 to-yellow-300 flex flex-col items-center justify-center px-6 py-12">
	<h1 class="text-6xl font-extrabold text-yellow-700 drop-shadow-lg mb-12 text-center tracking-wide">
	  🍔 Menú de McDonald's 🍟
	</h1>
  
	<div class="max-w-6xl grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 w-full">
	  {#each categories as category}
		<a href="{category.path}" 
		  class="relative block p-6 bg-white/80 backdrop-blur-lg rounded-3xl shadow-2xl hover:shadow-yellow-600/50 
		  hover:scale-105 transform transition-all duration-300 overflow-hidden group text-center">
		  
		  <div class="w-24 h-24 mx-auto bg-white rounded-full flex items-center justify-center shadow-lg mb-4 group-hover:scale-110 transition">
			<img src="{category.image}" alt="{category.name}" class="w-16 h-16">
		  </div>
		  
		  <span class="text-3xl font-bold text-yellow-800 group-hover:text-yellow-900 transition">
			{category.name}
		  </span>
		  
		  <div class="absolute inset-0 bg-yellow-500 opacity-0 group-hover:opacity-10 transition-all"></div>
		</a>
	  {/each}
	</div>
  </div>
  