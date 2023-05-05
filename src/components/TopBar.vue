<script setup >
import { ref,onMounted, computed } from 'vue';
import { useRouter } from 'vue-router';

import { useDark, useToggle } from '@vueuse/core';

const darkMode = useDark();
const toggleDark = useToggle(darkMode);
const router = useRouter()
const isMobile = ref(false);
const isTablet = ref(false);
const isDesktop = ref(false);
const menuVisible = ref(false);

const barMargin = computed(()=>{return (isDesktop.value===true)?"bigM":"ml-4";}) 
function openMenu(){
  menuVisible.value = true
  console.log("menu is visible")
}
function tog (){
  toggleDark()
  console.log("toggled: ", darkMode.value)
}

    onMounted(() => {
    });
</script>

<template>
     <div class="">
    <v-toolbar
      dark
      height="70"
      color="white"
    >
    <v-btn icon @click="openMenu" size="large">
    <font-awesome-icon  icon="fa-solid fa-bars"
     class="font-extrabold text-slate-900 text-2xl ml-1 lg:ml-1  mr-5 bigM" /> 
    </v-btn>   
      <div class="text-xl font-bold text-slate-700 ">African Biomeds Group</div>

      <v-spacer></v-spacer>

    </v-toolbar>
  </div>
  <v-dialog v-model="menuVisible"
        transition="dialog-bottom-transition"
        width="300"
      >
      <v-card class="bg-slate-50 dark:bg-slate-800">

          <p class="bg-slate-50 dark:bg-slate-800 text-2xl pt-4
          font-bold text-center mx-4 text-slate-900 dark:text-slate-50">
            Menu</p>
           <ul class="menux">
            <li v-on:click="{router.push('/'); menuVisible=false}" class="menu-item">
              <span><font-awesome-icon class="mr-2" icon="fa-solid fa-home" bounce /></span> Home
            </li> 

            <li v-on:click="{router.push('/activities'); menuVisible=false}" class="menu-item">
              <span ><font-awesome-icon class="mr-2" icon="fa-solid fa-puzzle-piece" bounce /></span> Activities
            </li>
            <li v-on:click="{router.push('/all'); menuVisible=false}" class="menu-item">
              <span><font-awesome-icon class="mr-2" icon="fa-solid fa-book" bounce /></span> All articles</li>
            <li class="menu-item" v-on:click="{router.push('/search'); menuVisible=false}">
              <span><font-awesome-icon class="mr-2" icon="fa-solid fa-magnifying-glass" bounce /></span> Search </li>
            <li class="menu-item" v-on:click="{router.push('/login'); menuVisible=false}">
              <span><font-awesome-icon class="mr-2" icon="fa-solid fa-blog" bounce /></span> Post an article</li>
           </ul>


            
          </v-card>
     
      </v-dialog>

</template>

<style scoped>
    .bigM{
        margin-left: 3%;
    }

    @media screen and (max-width: 850px) {
        .bigM{
        margin-left: 3%;
    }
    }

    .menux{
      @apply mb-4 mt-2 text-slate-900 dark:text-slate-50
    }
    .menu-item{
  @apply mx-5 font-bold text-lg  my-4 border-b-2 
    }
</style>
