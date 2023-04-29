<template>
    <div class="gallery">
        <img src="https://c4.wallpaperflare.com/wallpaper/761/1020/980/porsche-old-porsche-911-carrera-black-wallpaper-preview.jpg" alt="">
        <img src="https://c4.wallpaperflare.com/wallpaper/342/877/299/porsche-porsche-911-gt3-rs-porsche-911-gt3-car-wallpaper-preview.jpg" alt="">
        <img src="https://c4.wallpaperflare.com/wallpaper/937/428/36/porsche-rauh-welt-garage-hd-wallpaper-preview.jpg" alt="">
        <img src="https://c4.wallpaperflare.com/wallpaper/532/853/238/porsche-911-carrera-car-wallpaper-preview.jpg" alt="">
        <img src="https://c4.wallpaperflare.com/wallpaper/5/439/690/sunset-porsche-car-sunlight-wallpaper-preview.jpg" alt="">
        <img src="https://c4.wallpaperflare.com/wallpaper/838/837/161/porsche-964-rwb-cgi-porsche-964-rwb-cgi-hd-wallpaper-preview.jpg" alt="">
        <img src="" alt="">
        <img src="" alt="">
        <img src="" alt="">

    </div>
</template>

<script>
export default({
    name:"Gallery"
})
</script>

<style>
    .gallery{
        display: none;
        background-color: black;
        position: absolute;
        height: 99.8vh;
        width: 99.9vw;
        z-index: 3;
        overflow-y: scroll;
        animation: ease-in 2s;
    }
    .gallery::-webkit-scrollbar{
        width: 2px;
    }
    img{
        margin: 5%;
        width: 40%;
            
    }
</style>