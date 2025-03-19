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
    transition: 0.5s;
}

a:hover {
    color: #42b883;
}
</style>
