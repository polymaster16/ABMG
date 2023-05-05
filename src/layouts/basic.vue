<script lang="ts" setup>
import TopBar from '@/components/TopBar.vue';
import BottomMediaIconst from '@/components/BottomMediaIconst.vue';
</script>

<template>
    <main>
        <TopBar/>
       <slot></slot>
       <BottomMediaIconst/>
       

    </main>
</template>

<style lang="css" scoped>
    
</style>
