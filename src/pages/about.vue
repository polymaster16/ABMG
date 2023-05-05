<script setup>
import { Typed } from "@duskmoon/vue3-typed-js";

const options = {
    strings: ["Thank you for joining us in this journey."   ],
    loop: false,
    typeSpeed: 90,
 
  };
const route = useRoute()
</script>

<template> <div class="text-slate-900">
            <v-img height="120" width="auto" cover
            src="https://cdn.pixabay.com/photo/2013/02/09/04/15/doctor-79579_960_720.jpg">
       <div class="shade1 flex ">
            <div class="font-bold text-4xl text-white mt-12 ml-4">
            About us
        </div>
    </div>
        </v-img>

        <div class="text-xl mx-4 my-4 flex flex-row gap-4">
            <font-awesome-icon icon="fa-solid fa-feather-pointed" />

            <p>
                Welcome to our site! 
            </p>
        </div>

        <img 
        src="../assets/medsTeam.png" alt="" srcset="">

        <div class="text-xl mx-4 my-4 flex flex-row gap-4">
            <font-awesome-icon icon="fa-solid fa-feather-pointed" />

            <p>
                 We are a dedicated team of individuals who are passionate 
                about making a difference in the healthcare systems of developing countries 
                in Africa. 
            </p>
        </div>

        <div class="text-3xl text-center font-bold mb-3">
            Our Mission
        </div>
        <img 
        src="../assets/mission.jpg" 
        alt="" srcset="">

        <div class="text-xl mx-4 my-4 flex flex-row gap-4">
            <font-awesome-icon icon="fa-solid fa-feather-pointed" />

            <p>
                Our mission is to provide basic medical hygiene education 
                and training to healthcare professionals, as well as to supply
                 and repair medical equipment, in order to create a sustainable 
                 and self-sufficient healthcare system for the underserved and 
                 marginalized individuals in these areas.
            </p>
        </div>

        <div class="text-xl mx-4 my-4 flex flex-row gap-4">
            <font-awesome-icon icon="fa-solid fa-feather-pointed" />

            <p>
                Our goal is to improve the quality of healthcare and provide 
                a clean and safe environment for healing. 
                We believe that everyone deserves access to quality healthcare,
                 and we are committed to making that a reality, one life at a time.
            </p>
        </div>


        <div class="mx-8">
<Typed :options="options">
    <div class="typing text-2xl text-slate-900 font-bold text-center mt-5"></div>
    </Typed>
</div>

<div class="text-3xl text-center font-bold mb-3">
    Founder’s Story
        </div>
        <img 
        src="https://africanbiomedgroup.org/wp-content/uploads/2022/10/Founder-pic-African-Biomed-Group-300x225.jpg" 
        alt="" srcset="">

</div>
</template>

<style scoped>
    
</style>
