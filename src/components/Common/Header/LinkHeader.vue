<template>
    <a>
        {{ title }}
    </a>
</template>

<script lang="ts" setup>

defineProps<{
    title: string
}>()
</script>

<style lang="css" scoped>

a {
    text-decoration: none;
    color: white;
    cursor: pointer;
    font-weight: 600;
    font-size: large;
    transition: 0.3s;
}

a:hover {
    color: #42b883;
}
</style>
