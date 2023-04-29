<script setup>

</script>

<template>
  <div class="container1">
    <img src="./assets/map-world-map-wallpaper-a9b0588db1da2d9b960778af10a1d60d.jpg" alt="background"     class="container2">
      
    
    <Gallery />
    <Header />
    <Sidebar @update="updateCurrent" :cars="cars" :current="current"/>
    <Card @next="nextItem" @prev="preItem" :cars="cars" :current="current" />
    <!-- <footer></footer> -->
  </div>
  
</template>

<script >
import Card from './components/icons/Card.vue';
import Header from './components/icons/Header.vue';
import Sidebar from './components/icons/Sidebar.vue';
import Gallery from './components/Gallery.vue'

export default ({
  name:'App',

  components: {
    Header,
    Sidebar,
    Card,
    Gallery,
  },

  data(){
    return{
      current: 0,

      cars: [
        {
          id : 1,
          model: "TYCAN TURBO",
          picture: "https://www.porsche-moscow.ru/photos/cars/custom/456405_5PNaIMT0p21d1TJfsHBa4ebwrjVFDeGj.jpg.optimized.png",
          power: "460 kW/625 PS",
          time: "3.2",
          speed: "260"
        },
        {
          id : 2,
          model: "911 GT3 RS",
          picture: "https://files.porsche.com/filestore/image/multimedia/none/992-gt3-rs-modelimage-sideshot/model/cfbb8ed3-1a15-11ed-80f5-005056bbdc38/porsche-model.png",
          power: "386 kW/525 PS",
          time: "3.2",
          speed: "296"
        },
        {
          id : 3,
          model: "911 GT3",
          picture: "https://files.porsche.com/filestore/image/multimedia/none/992-gt3-modelimage-sideshot/model/765dfc51-51bc-11eb-80d1-005056bbdc38/porsche-model.png",
          power: "375 kw/510 PS",
          time: "3.4",
          speed: "318km/h"
        },
        {
          id : 4,
          model: "911 TURBO",
          picture: "https://files.porsche.com/filestore/image/multimedia/none/911-tu-modelimage-sideshot/model/fe21bac9-833c-11eb-80d3-005056bbdc38/porsche-model.png",
          background:"https://r4.wallpaperflare.com/wallpaper/469/346/508/map-world-map-wallpaper-a9b0588db1da2d9b960778af10a1d60d.jpg" ,
          power: "427 kW/580 PS",
          time: "2.8",
          speed: "320"
        },
        {
          id : 5,
          model: "TYCAN 4S",
          picture: "https://files.porsche.com/filestore/image/multimedia/none/j1-taycan-modelimage-sideshot/model/e36a18ca-fffb-11eb-80dd-005056bbdc38/porsche-model.png",
          background:"https://r4.wallpaperflare.com/wallpaper/120/617/113/golden-yellow-library-map-old-time-map-wallpaper-d6ea2c94e2b84db62823fb62287a0d74.jpg" ,
          power: "320 kW/435 PS",
          time: "4.0",
          speed: "250"
        },
        {
          id : 6,
          model: "TYCAN GTS",
          picture: "https://files.porsche.com/filestore/image/multimedia/none/j1-taycan-gts-modelimage-sideshot/model/0f46e1ba-43b4-11ec-80e2-005056bbdc38/porsche-model.png",
          background:"./assets/map-world-map-wallpaper-a9b0588db1da2d9b960778af10a1d60d.jpg" ,
          power: "380 kW/517 PS",
          time: "3.7",
          speed: "250"
        },
        {
          id : 7,
          model: "718 SPYDER",
          picture: "https://files.porsche.com/filestore/image/multimedia/none/982-718spyder-modelimage-sideshot/model/d9552a39-8616-11e9-80c4-005056bbdc38/porsche-model.png",
          background:"./assets/map-world-map-wallpaper-a9b0588db1da2d9b960778af10a1d60d.jpg" ,
          power: "309 kW/420 PS",
          time: "4.4",
          speed: "310"
        },
        {
          id : 8,
          model: "PANAMERA 4",
          picture: "https://files.porsche.com/filestore/image/multimedia/none/971-g2-2nd-4-modelimage-sideshot/model/dc348883-d31f-11ea-80cc-005056bbdc38/porsche-model.png",
          background:"./assets/map-world-map-wallpaper-a9b0588db1da2d9b960778af10a1d60d.jpg" ,
          power: "243 kW/330 PS",
          time: "5.3",
          speed: "268",
        }
    ]
    }
    
  },
  methods:{
        nextItem() {
            this.current==7? this.current=0: this.current++;
            console.log(this.current)
        },
        preItem() {
            this.current==0? this.current=7: this.current--;
            console.log(this.current)
        },
        updateCurrent(id){
          this.current= id-1;
        }
      },
})

</script>


<style scoped>
  .container1{
    height: 100%;
    width: 100%;
    padding: 0;
    margin: 0px;
    color: white;
    background-image: linear-gradient(145deg, rgb(214, 223, 226), rgb(148, 163, 177),  rgb(79, 83, 92), rgb(137, 163, 172));
    /* background: url(https://c4.wallpaperflare.com/wallpaper/644/305/118/pattern-black-gradient-texture-wallpaper-preview.jpg) no-repeat center; */
    background-size: cover;
    border: 1px solid black;
  }
  .container2{
    position: absolute;
    height: 99.9%;
    width: 99.9vw;
    margin: 0px;
    clip-path: polygon(68% 0%, 98% 0%, 78% 100%, 48% 100%);
    /* --mask: radial-gradient(circle at var(--x, 100%) var(--y, 50%), black 25%, transparent 0);
    -webkit-mask-image: var(--mask);
	  mask-image: var(--mask); */
  }
</style>
