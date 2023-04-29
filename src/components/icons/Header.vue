<template>
    <header>
      <ul>
        <li>
            <img class="logo" src="../../assets/porsche-logo-16.png" alt="">
            
        </li>
        <li>SHOP</li>
        <li>MORE</li>
        <li><button class="btn btn-secondary">RPC DEALER</button></li>
        <li><button @click="gallery"  class="btn btn-light " >VIEW GALLERY</button></li>
      </ul>
    </header>
</template>

<script>

export default ({
    name:'Header',
    methods:{
      gallery(){
        document.querySelector('.gallery').style.display= 'inline';
      }
    }
})
</script>


<style scoped>


ul{
    font-size: 0.9rem;
    position: absolute;
    margin: 0;
    padding: 10px;
    right: 80px;
  }
  li{
    display: inline-block;
    margin: 30px;
  }
  button{
    /* margin-left: 30px; */
    margin-right: 0;
  }
  .logo{
    height: 50px;
  }
</style>