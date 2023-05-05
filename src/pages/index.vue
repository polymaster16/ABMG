
<script setup>
import TopBar from "@/components/TopBar.vue";
import { Typed } from "@duskmoon/vue3-typed-js";
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import logo from '../assets/logo.png'

const name = ref("William") 
const my = useRouter() 

const slides = ref([
{
  img: logo
},
{
  img:"https://africaintherockies.org/wp-content/uploads/2019/04/Disabled-in-Africa-1024x683.jpg"
},
{
  img:"https://pbs.twimg.com/media/FrWpFiZWYAAk3DR?format=jpg&name=4096x4096"
},
{
  img:'https://cdn.pixabay.com/photo/2016/01/14/02/48/girl-1139277_960_720.jpg'
}

  ])

const options = {
    strings: ["Saving Lives", "The African Biomed's group story!"],
    loop: false,
    typeSpeed: 90,
 
  };
</script>

<template>
<div class="img1">
  <div class="shade1">
    <div>
<carousel dir="rtl" :transition="500"  :autoplay="2000" v-bind:wrap-around="true">
    <slide v-for="x in slides" :key="x.img">
      <img class="circularLogo" :src="x.img">
    </slide>
  </carousel>
</div>

<Typed :options="options">
    <div class="typing text-3xl text-slate-100 font-bold text-center mt-5"></div>
    </Typed>

    <div class="center my-4 scara">
    <v-btn rounded="pill" color="green" @click="my.push('/about')">
      <strong>LEARN MORE</strong>
    </v-btn>
  </div>

  </div>
</div>



      <div class="mx-5">
    <div class="">
  
    </div>
    <div class="center my-4">
    <v-btn color="pink" @click="my.push('/about')">About</v-btn>
  </div>
  <div class="center my-4">
    <v-btn color="green" @click="my.push('/post/')">Post</v-btn>
  </div>
</div>
</template>

<style lang="" scoped>
    
</style>

    
