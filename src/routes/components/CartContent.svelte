<script lang="ts">
    // ใช้รับค่า cartItems และฟังก์ชันต่าง ๆ จาก CartPage
    export let cartItems;
    export let updateQuantity: (id: number, newQuantity: number) => void;
    export let removeItem: (id: number) => void;
  </script>
  
  <div class="space-y-4 max-h-[300px] overflow-scroll">
    {#each $cartItems as item (item.id)}
      <div class="flex bg-gray-100 p-4 rounded-lg items-center">
        <div class="w-1/6 mr-4">
          <img src={item.image} alt={item.name} class="w-full object-cover" />
        </div>
  
        <div class="w-2/3 space-y-2">
          <div class="text-gray-600 uppercase text-xs">{item.articleNr}</div>
          <div class="font-semibold text-lg">{item.name}</div>
          <div class="text-gray-500 text-sm">
            <span class="uppercase">Color:</span> {item.color}<br>
            <span class="uppercase">Size:</span> {item.size}
          </div>
  
          <div class="flex items-center space-x-2">
            <input 
              type="number" 
              bind:value={item.quantity} 
              on:change={() => updateQuantity(item.id, item.quantity)}
              min="1" 
              class="w-12 text-center border border-black rounded" 
            />
            <button 
              on:click={() => updateQuantity(item.id, item.quantity)}
              class="bg-black text-white px-3 py-1 rounded text-sm"
            >
              Update
            </button>
            <span class="text-gray-600">x {item.price} SEK</span>
          </div>
        </div>
  
        <div class="w-1/6 text-right space-y-2">
          <div class="font-semibold text-lg">{item.price * item.quantity} SEK</div>
          <button 
            on:click={() => removeItem(item.id)}
            class="bg-red-200 text-black px-3 py-1 rounded-full text-sm"
          >
            Remove
          </button>
        </div>
      </div>
    {/each}
  </div>
  