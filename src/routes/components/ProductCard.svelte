<script>
  export let product;
</script>

<div
  class="max-w-xs w-full  bg-white shadow-lg rounded-md overflow-hidden group hover:bg-gray-100 transition ease-in-out duration-300"
>
  <a href={product.link || "#"} class="block">
    <!-- Product Image -->
    <img
      src={product.image || "https://via.placeholder.com/150"}
      alt={product.title || "Product Image"}
      class="w-full h-48 object-cover group-hover:opacity-80 transition-opacity duration-300"
    />

    <div class="p-4">
      <!-- Product Title -->
      <h3
        class="text-lg font-semibold text-gray-800 group-hover:text-blue-500 transition-colors duration-300"
      >
        {product.title || "Default Product Title"}
      </h3>

      <!-- Product Description -->
      <p class="text-gray-600 text-sm mt-2 truncate">
        {product.description || "No description available"}
      </p>

      <!-- Price and View Button -->
      <div class="mt-4 flex items-center justify-between">
        <span class="text-xl font-bold text-gray-900"
          >{product.price || "฿0"}</span
        >
        <button
          class="px-4 py-2 bg-blue-500 text-white rounded-md hover:bg-blue-600 transition-colors duration-300"
        >
          ดูรายละเอียด
        </button>
      </div>

      <!-- Additional Info Section -->
      <div class="mt-2 text-sm text-gray-500">
        <span>{product.additionalInfo || "No additional info"}</span>
      </div>
    </div>
  </a>

  <!-- Discount Tag -->
  {#if product.discount !== undefined}
    <div
      class="absolute top-2 left-2 bg-red-500 text-white text-xs px-2 py-1 rounded-full"
    >
      -{product.discount}%
    </div>
  {/if}
</div>
