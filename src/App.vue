<script setup>
    import VHeader from './components/VHeader.vue';
    import VFooter from './components/VFooter.vue'
    import VAbout from './components/VAbout.vue';
    import VRool from './components/VRool.vue';
    import VGame from './components/VGame.vue';
</script>

<template>
   <div class="container-fluid">
        <v-header></v-header>
        <div class="stroke1 z-0"></div>
        <main role="main" class="main">
            <v-about></v-about>
            <v-rool></v-rool>
            <v-game></v-game>
        </main>
        <div class="stroke2"></div>
        <v-footer></v-footer>
        
    </div>
</template>

<style scoped>

</style>
