<script setup>

</script>

<template>
    <section>
        <HomeHero />
        <div class="relative">
            <div class="navGradienBottom"></div>
        </div>
        <HomeQuestionText />
        <HomeEmployerEmployee />
        <HomeSummary />
    </section>
</template>



<style  scoped>
.navGradienBottom {
    position: absolute;
    width: 100%;
    height: 35.7rem;
    bottom: -17.2rem;
    background: linear-gradient(180deg, rgba(6, 19, 26, 0) 0%, #06131A 51.3%, rgba(6, 19, 27, 0) 100%);
    transform: matrix(-1, 0, 0, 1, 0, 0);
}
</style>