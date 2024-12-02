<script>
  import Icon from "@iconify/svelte";
</script>

<nav class=" p-4 ">

  <div class="flex justify-around items-center ">

    <div class="text-white font-bold text-xl">
      <a href="/Home"><img src="/logo.png" alt="logo" class="w-24" /></a>
    </div>

    <!-- Search Bar -->
    <form class=" ">
      <div class="flex  px-10">

        <div class=" w-[800px] ">
          <input
            type="search"
            id="search-dropdown"
            class="block p-2.5 pl-10 w-full text-sm text-gray-900 bg-gray-200 "
            placeholder="Search"
            required
          />
        </div>

        <button
            type="submit"
            class=" top-0 right-0 p-2.5 text-sm font-medium h-10 text-white bg-blue-700  hover:bg-blue-800 "
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
      <a href="/" class="flex items-center ">
        <button
          class=" top-0 right-0  text-sm font-medium h-10 text-blue-800 hover:bg-gray-800 "
        >
          <Icon icon="ic:outline-shopping-cart"class="w-full h-full" />
        </button>
      </a>

  </div>
</nav>

<style>
  nav {
    background-color: #ffffff;
    position: sticky;
    top: 0;
    width: 100%;
    z-index: 1000; /* ทำให้ navbar อยู่บนสุด */
  }
</style>
