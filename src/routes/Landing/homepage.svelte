<script lang="ts">
    import Carousel from '../components/Carousel.svelte';

    const carouselImages = [
        "/A.jpg",
        "/B.jpg",
        "/C.jpg",
        "/D.jpg",
        "/E.jpg",   
        "/F.jpg"
    ];
</script>
<div class="bg-white min-h-screen"> 

    <div >
        <div class="pl-[460px] py-1 ">
            <h1>Ads</h1>
        </div>
        <Carousel images={carouselImages} />
        
    </div>
    
    <div>
        
    
    </div>

</div>

