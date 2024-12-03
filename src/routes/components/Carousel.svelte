<!-- Carousel.svelte -->
<script lang="ts">
    export let images: string[] = [
        "https://fakeimg.pl/2000x800/0079D8/fff/?text=Without",
        "https://fakeimg.pl/2000x800/DA5930/fff/?text=JavaScript",
        
    ];

    let currentSlide = 0;

    function nextSlide() {
        currentSlide = (currentSlide + 1) % images.length;
    }

    function prevSlide() {
        currentSlide = (currentSlide - 1 + images.length) % images.length;
    }

    function goToSlide(index: number) {
        currentSlide = index;
    }
</script>

<div class="relative shadow-md  overflow-hidden justify-items-center">
    <div class="relative w-[988px] h-[400px]">
        {#each images as image, index}
            <div 
                class="absolute w-full h-full transition-opacity duration-600 ease-out"
                class:opacity-100={index === currentSlide}
                class:opacity-0={index !== currentSlide}
            >
                <img 
                    src={image} 
                    alt="Carousel slide {index + 1}" 
                    class="block w-full h-full object-cover"
                />
            </div>
        {/each}

        <!-- Previous Button -->
        <button 
            on:click={prevSlide}
            class="absolute left-[2%] top-1/2 -translate-y-1/2 w-10 h-10 bg-black/30 hover:bg-black/80 rounded-full text-white flex items-center justify-center text-2xl z-10"
        >
            ‹
        </button>

        <!-- Next Button -->
        <button 
            on:click={nextSlide}
            class="absolute right-[2%] top-1/2 -translate-y-1/2 w-10 h-10 bg-black/30 hover:bg-black/80 rounded-full text-white flex items-center justify-center text-2xl z-10"
        >
            ›
        </button>

        <!-- Indicators -->
        <div class="absolute bottom-[2%] left-0 right-0 flex justify-center space-x-2 z-10">
            {#each images as _, index}
                <button 
                    on:click={() => goToSlide(index)}
                    class="text-3xl"
                    class:text-blue-500={index === currentSlide}
                    class:text-white={index !== currentSlide}
                >
                    •
                </button>
            {/each}
        </div>
    </div>
</div>