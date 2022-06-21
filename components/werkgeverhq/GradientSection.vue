<script setup>

</script>
<template>
    <section class="relative">
        <div class="bottomGradient"></div>
    </section>
</template>



<style scoped>
section{
    background: rgb(6, 19, 26);
    height: 40rem;
}
.bottomGradient {
    background: linear-gradient(180deg, rgba(6, 19, 26, 0) 0%, #06131A 100%);
transform: matrix(-1, 0, 0, 1, 0, 0);
    position: relative;;
    z-index: 2;
    width: 100%;
    top: -21rem;
    height: 23rem;
}
</style>