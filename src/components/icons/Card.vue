`"volar.inlayHints.eventArgumentInInlineHandlers": false`

<template>
        <div class="card1" :cars="cars" :current="current">   
        <h2>/ PORSCHE {{cars[current].model}}</h2>
        <transition name="slide-up2" mode="out-in">
            <h1 class="name" :key="current">{{cars[current].model}}</h1>
        </transition>
        <transition name="slide-up" mode="out-in">
            <img  :src="cars[current].picture" alt="porche" :key="current">
        </transition>
        
        <button @click="onClickNxt()" class="ind ind-nxt">&gt</button>
        <button @click="onClickPre()" class="ind ind-pre">&lt</button>
        
        <ul class="ul-2">
            <li>
                {{cars[current].power}} <br>
                <p>power</p>
            </li>
            <li>
                {{cars[current].speed}} km/h <br>
                <p>speed</p>
            </li>
            <li>
                {{cars[current].time}} s<br>
                <p>time</p>
            </li>
        </ul>

    </div>
   
</template>
<script>
import { Transition, TransitionGroup } from 'vue';

export default ({
    name: 'Card',
    props: {
        cars: Array,
        current: Number,
    },
    components: {
        Transition,
        TransitionGroup,
    },
    methods:{
        onClickNxt() {
            this.$emit('next');
        },
        onClickPre() {
            this.$emit('prev')
        }
    },
    
});
</script>

<style  scoped>


    .card1{
    margin-top:100px;
    margin-left: 250px;
    height: 80%;
    width: 80%;
    bottom: 0px;
    padding: 5%;
    align-items: center;
    font-family: 'Gruppo', cursive;
    /* background-color: rgba(255, 255, 255, 0.151);
    backdrop-filter: blur(10px); */

  }
  img{
    position: absolute;
    max-width: 50%;
    max-height: 70%;
    margin-left: 7%;
    /* margin-top: 80px; */
    top: 25%;
    /* right: 18%; */
    z-index: 2;
    /* background-color: rgb(70, 134, 190); */
    transition:width 2s
  }
  .name{
    font-family: 'Gruppo', cursive;
    position: absolute;
    font-size: 950%;
    font-weight:100;
    margin-left: auto;
    margin-right: auto;
    margin-top: 3%;
    top: 28%;
    left: 23%;

    z-index: 1;
    }
    li{
        display: inline-block;
        margin-right: 60px;
    }
    .ind{
        position: absolute;
        height: 50px;
        color: rgb(233, 231, 231);
    }
    .ul-2{
        position: absolute;
        bottom: 0px;
        left: 250px;
        font-size: 1.3rem;
    }
    .ind{
        position: absolute;
        color: rgb(204, 204, 204);
        font-size: 2rem;
        line-height: 1;
        bottom: 35%;
        background-color: rgba(0, 0, 0, 0.123);
        border: none;
    }
    .ind-nxt{
        right: 3%;
    }
    .ind-pre{
        left: 18%;
    }
    h2{
        font-size: 1.2rem;
    }
    p{
        font-size: 1rem;
    }
    

.slide-up-enter-active,
.slide-up-leave-active {
  transition: all 0.15s ease-out;
}

.slide-up-enter-from {
  opacity: 0;
  transform: translateX(-30px);
}

.slide-up-leave-to {
  opacity: 0;
  transform: translateX(30px);
}
.slide-up2-enter-active,
.slide-up2-leave-active {
  transition: all 0.25s ease-out;
}

.slide-up2-enter-from {
  opacity: 0;
  transform: translateX(-30px);
}

.slide-up2-leave-to {
  opacity: 0;
  transform: translateX(30px);
}

@media(max-width: 1440px){
  .name{
    font-size: 850%;
  }
  .img{
    margin-left: 3%;
  }

}
</style>