<script>
  let password = "";
  let toggle = false;
</script>

<div
  class="min-h-screen py-48 bg-gradient-to-r from-indigo-500 to-sky-500 flex items-center justify-center"
>
  <div class="bg-gray-100 flex rounded-2xl shadow-lg max-w-3xl p-5">
    <!-- form -->
    <div class="md:w-1/2 px-16 py-10 md:px-16">
      <h2 class="text-2xl font-bold text-[#002D74]">Login</h2>
      <p class="text-sm mt-4 text-[#284a82]">
        &nbsp;&nbsp;&nbsp;If you already a member , log in
      </p>

      <form action="" class="flex flex-col gap-4">
        <input
          class="p-2 mt-8 rounded-xl border"
          type="text"
          placeholder="Username"
        />
        <div class="relative">
          <input
            class="p-2 rounded-xl border w-full"
            type={ toggle ? "text" : "password"}
            placeholder="Passsword"
            bind:value={password}
          />
          <button
            class="bi bi-eye absolute top-1/2 right-3 -translate-y-1/2"
            on:click={() => {
              toggle = !toggle;
              console.log(toggle)
            }}>
            {#if toggle}
            <!-- Eye (open) icon -->
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class=" bi bi-eye absolute top-1/2 right-3 -translate-y-1/2"
              viewBox="0 0 16 16">
              <path d="M16 8s-3-5.5-8-5.5S0 8 0 8s3 5.5 8 5.5S16 8 16 8zM1.173 8a13.133 13.133 0 0 1 1.66-2.043C4.12 4.668 5.88 3.5 8 3.5c2.12 0 3.879 1.168 5.168 2.457A13.133 13.133 0 0 1 14.828 8c-.058.087-.122.183-.195.288-.335.48-.83 1.12-1.465 1.755C11.879 11.332 10.119 12.5 8 12.5c-2.12 0-3.879-1.168-5.168-2.457A13.134 13.134 0 0 1 1.172 8z" />
              <path d="M8 5.5a2.5 2.5 0 1 0 0 5 2.5 2.5 0 0 0 0-5zM4.5 8a3.5 3.5 0 1 1 7 0 3.5 3.5 0 0 1-7 0z" />
            </svg>
            {:else}
            <!-- Eye (closed) icon -->
            <svg 
              xmlns="http://www.w3.org/2000/svg" 
              width="16" 
              height="16" 
              fill="currentColor" 
              class="bi bi-eye-slash absolute top-1/2 right-3 -translate-y-1/2" 
              viewBox="0 0 16 16"
              >
                <path d="M13.359 11.238C15.06 9.72 16 8 16 8s-3-5.5-8-5.5a7 7 0 0 0-2.79.588l.77.771A6 6 0 0 1 8 3.5c2.12 0 3.879 1.168 5.168 2.457A13 13 0 0 1 14.828 8q-.086.13-.195.288c-.335.48-.83 1.12-1.465 1.755q-.247.248-.517.486z"/>
                <path d="M11.297 9.176a3.5 3.5 0 0 0-4.474-4.474l.823.823a2.5 2.5 0 0 1 2.829 2.829zm-2.943 1.299.822.822a3.5 3.5 0 0 1-4.474-4.474l.823.823a2.5 2.5 0 0 0 2.829 2.829"/>
                <path d="M3.35 5.47q-.27.24-.518.487A13 13 0 0 0 1.172 8l.195.288c.335.48.83 1.12 1.465 1.755C4.121 11.332 5.881 12.5 8 12.5c.716 0 1.39-.133 2.02-.36l.77.772A7 7 0 0 1 8 13.5C3 13.5 0 8 0 8s.939-1.721 2.641-3.238l.708.709zm10.296 8.884-12-12 .708-.708 12 12z"/>
            </svg>
           {/if}
          </button>
          
        </div>
        <div class="mt-1 text-right">
          <p class=" text-sm">
            <a href="#" class="text-gray-600 hover:underline ">Forgot your password?</a>
          </p>
        </div>
        <button
          class="bg-[#002D74] hover:bg-[#0e213d] rounded-xl text-white py-2"
        >
          Login
        </button>

        <div class="mt-5 text-center">
          <p class="text-gray-600 text-sm">
            If you don't have an account 
            <a href="/user-register.svelte" class="text-blue-500 hover:underline">Register</a>
          </p>
        </div>

      </form>
    </div>

    <!-- image -->
    <div class="md:block hidden w-1/2 ">
      <img class=" rounded-2xl" src="/login_img.jpg" alt="" />
    </div>
  </div>
</div>
