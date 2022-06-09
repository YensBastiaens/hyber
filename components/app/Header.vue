<script setup>

</script>

<template>
    <div class="flex justify-center">
        <nav class="container absolute flex flex-row justify-between items-center pt-[3.5rem] z-[1]">
            <img class="flex items-center" src="~/assets/images/logo/hyber.svg" alt="logo">
            <div class="flex gap-[2.5rem] font-bold text-white">
                <a href="#">Werkgever HQ</a>
                <a href="#">Werknemerskwartier</a>
                <a href="#">Productiehal</a>
                <a href="#">Receptie</a>
            </div>
        </nav>
        <div class="navGradientTop"></div>
        <div class="navGradienBottom"></div>
    </div>

</template>

<style scoped>
.navGradientTop {
    background: linear-gradient(180deg, rgba(6, 19, 26, 0.6) 0%, rgba(6, 19, 26, 0) 100%);
    position: absolute;
    width: 100%;
    height: 35rem;
    z-index: 0;
}

.navGradienBottom {
    position: absolute;
    width: 100%;
    height: 70vh;
    bottom: 87vh;
    background: linear-gradient(180deg, rgba(6, 19, 26, 0) 0%, #06131A 51.3%, rgba(6, 19, 27, 0) 100%);
    transform: matrix(-1, 0, 0, 1, 0, 0);
}
</style>