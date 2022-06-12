<script setup>

</script>

<template>
    <div class="flex justify-center relative ">
        <nav class="container absolute flex flex-row justify-between items-center pt-[3.5rem] z-[2]">
            <img class="flex items-center" src="~/assets/images/logo/logoWhite.svg" alt="logo">
            <div class="flex gap-[2.5rem] font-bold text-white">
                <a href="#">Werkgever HQ</a>
                <a href="#">Werknemerskwartier</a>
                <a href="#">Productiehal</a>
                <a href="#">Receptie</a>
            </div>
            
        </nav>
        <div class="navGradientTop"></div>
    </div>

</template>

<style scoped>
.navGradientTop {
    background: linear-gradient(180deg, rgba(6, 19, 26, 0.6) 0%, rgba(6, 19, 26, 0) 100%);
    width: 100%;
    height: 35rem;
    z-index: 0;
    position: fixed;
}


</style>