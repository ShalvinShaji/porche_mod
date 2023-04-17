<template>
    <div class="sidebar">
        <div class="icon-list">
            <ul class="ul-1" :key ="car.id" v-for="car in cars" >
            <li @click="changecurrent(car.id)"> <img :class="[car.id==current+1? 'bordered' : '', 'icon']" :src="car.picture" alt="pic"></li>
        </ul>
        </div>
        
        <!-- <ul class="ul-2">
            <li>Classic</li>
            <li>Turbo</li>
            <li>Roadster</li>
        </ul> -->
        <span class="number">0{{current+1}}</span><span>/08</span>
    </div>
</template>

<script>

export default ({
    name: 'Sidebar',
    props: {
        cars: Array,
        current: Number,
    },
    methods:{
        changecurrent(id){
            this.$emit('update', id)
        }
    }
});
</script>



<style scoped>
    .sidebar{
        width: 200px;
        height: 100%;
        float: left;
        padding-left: 30px;
        padding-top: 30px;
        font-family: 'Gruppo', cursive;
          background-color: rgba(255, 255, 255, 0.062);
          /* color: rgb(33, 102, 102); */
        }
    .ul-1{
        list-style-type: none;
        /* margin-bottom: 50px; */
    }
    .icon-list{
        /* border: 1px solid black; */
        height: 400px;
        overflow:auto ;
        margin-bottom: 50px;
         
        /* backdrop-filter: blur(10px);  */
    }
    .icon-list::-webkit-scrollbar{
        width: 1em;
    }
    .icon{
        width: 80px;
        /* margin-bottom: 10px; */
    }
    .number{
        font-size: 6rem;
        line-height: 1;
        margin-left: 20px;
        
    }
    .ul-2{
        list-style-type: circle;
        margin-left: 30px;
        margin-bottom: 45px;
    }
    .bordered{
        border-bottom: 2px  solid rgba(255, 255, 255, 0.479);
       
    }
</style>