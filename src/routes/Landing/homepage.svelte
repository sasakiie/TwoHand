<script lang="ts">
    import Carousel from '../components/Carousel/Carousel.svelte';
    import Page from "../components/SellingObj.svelte"
    import Productlist from "../components/Product.svelte"
    const carouselImages = [
        "/A.jpg",
        "/B.jpg",
        "/C.jpg",
        "/D.jpg",
        "/E.jpg",   
        "/F.jpg"
    ];
</script>
<div class="bg-Black min-h-screen justify-items-center"> 

    <div >
        <div class="pl-[460px] py-1 ">
            <h1>Ads</h1>
        </div>
        <Carousel images={carouselImages} />
    </div>
    
    <div class="justify-items-center">
        <Page/>
    </div>

    <div class=" bg-white justify-items-center w-3/4 h-[55px] content-center border-b-4 border-orange-800">
        <div class=" ">
            <span class="text-orange-700">สินค้าแนะนำประจำวัน</span>
        </div>
    </div>
    <div>
        <Productlist/>
    </div>

</div>

