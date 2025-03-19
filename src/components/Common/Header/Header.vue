<template>
    <header>
        <div>
            <img src="/src/assets/vue.svg" alt="">
        </div>
        <div class="nav_bar">
            <template v-for="link in NavLink">
                <LinkHeader :title="link" />
            </template>
        </div>
    </header>
</template>

<script lang="ts" setup>
import LinkHeader from './LinkHeader.vue';


const NavLink = [
    "Home",
    "Profil",
    "Contact"
]
</script>

<style lang="css" scoped>
header {
    height: 100px;
    width: 100%;
    background-color: #35495e;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    box-sizing: border-box
}

.nav_bar {
    width: 100%;
    display: flex;
    gap: 20px;
    justify-content: center;
    align-items: center;
}

</style>