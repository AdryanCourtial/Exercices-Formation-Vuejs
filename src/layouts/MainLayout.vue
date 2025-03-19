<template>
    <div>
        <Header />
            <slot />
        <Footer />
    </div>
</template>

<script lang="ts" setup>
import Header from '../components/Common/Header/Header.vue';
import Footer from '../components/Common/Footer.vue';

</script>

<style lang="css" scoped>

</style>
