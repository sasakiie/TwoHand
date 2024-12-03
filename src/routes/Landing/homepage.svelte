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
<div>
    <div>
        <h1>แนะนำสำหรับคุณ</h1>
    </div>
    <Carousel images={carouselImages} />
    <div>
        <h1>แนะนำสำหรับคุณ</h1>
    </div>
</div>
<!-- <main class="bg-[url('https://digital.bnint.com/filelib/s9/photos/white_wood_4500x3000_lo_res.jpg')] min-h-screen">
    
</main> -->