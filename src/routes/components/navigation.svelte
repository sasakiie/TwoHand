<script>
  import Icon from "@iconify/svelte";
  import CartPage from "../components/CartPage.svelte";

  let isCartOpen = false;

  function toggleCart() {
    isCartOpen = !isCartOpen;
  }
</script>

<nav class="p-2 drop-shadow-md">
  <div class=" flex justify-end space-x-[100px] mb-[1px] mt-[1px]">
    <a href="/Authentication">register</a>
    <a href="/Authentication">register</a>
    <a href="/Authentication">register</a>
    <a href="/Authentication">register</a>
  </div>
  <div class="">
    <div class="flex justify-around items-center">
      <div class="text-white font-bold text-xl">
        <a href="/Landing"><img src="/logo.png" alt="logo" class="w-24" /></a>
      </div>

      <!-- Search Bar -->
      <form class=" ">
        <div class="flex px-10">
          <div class=" w-[800px]">
            <input
              type="search"
              id="search-dropdown"
              class="block p-2.5 pl-10 w-full text-sm text-gray-900 bg-gray-200"
              placeholder="Search"
              required
            />
          </div>

          <button
            type="submit"
            class=" top-0 right-0 p-2.5 text-sm font-medium h-10 text-white bg-blue-700 hover:bg-blue-800"
          >
            <svg
              class="w-4 h-4"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 20 20"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
              />
            </svg>
            <span class="sr-only">Search</span>
          </button>
        </div>
      </form>

      <!-- Cart icon -->
      <button class="relative" on:click={toggleCart}>
        <Icon icon="ic:outline-shopping-cart" class="w-8 h-8 text-blue-800" />
      </button>
    </div>
  </div>
</nav>
<!-- Popup Cart -->
{#if isCartOpen}
  <div
    class="fixed inset-0 z-50 bg-gray-800 bg-opacity-50 flex items-center justify-center"
  >
    <div class="bg-white rounded-lg shadow-lg w-3/4 max-w-2xl relative">
      <!-- Close Button -->
      <button
        class="absolute top-2 right-2 text-gray-500"
        on:click={toggleCart}
      >
        ✖
      </button>

      <!-- Cart Page Content -->
      <CartPage />
    </div>
  </div>
{/if}

<style>
  nav {
    background-color: #ffffff;
    position: sticky;
    top: 0;
    width: 100%;
    z-index: 1000; /* ทำให้ navbar อยู่บนสุด */
  }
</style>
