<script setup>

const props = defineProps({
    text: {
        type: String,
        default: 'text'
    },
    url: {
        type: String,
        default: '/'
    }
})

</script>

<template>
    <a class="
    text-black
    font-bold
    bg-blue
    py-[15px]
    px-[40px]
    rounded-[1rem]
    " :href="url">
        {{ props.text }}
    </a>
</template>

<style scoped>

</style>