<script lang="ts">
    const { title, description, price, image } = $props<{
      title: string;
      description: string;
      price: string;
      image: string;
    }>();
  </script>
  
  <div class="border rounded-lg shadow-lg p-4 bg-white">
    <img src={image} alt={title} class="w-full h-40 object-cover rounded-lg">
    <h2 class="text-xl font-bold mt-2">{title}</h2>
    <p class="text-gray-600">{description}</p>
    <span class="text-lg font-semibold text-red-500">${price}</span>
  </div>
  