<template>
    <div>
        <div class="container1">
            <div class="hero1 panel bg-red-400">
                <img class="right-[58vh] top-[14.5vh] absolute z-[2]" src="~/assets/images/elements/fish.png" alt="vis">
                <div class="flex justify-center">
                    <h1 class="pt-[15vh] text-white text-center  absolute z-[1] ">Nee, serieus. <br>Echt overal.</h1>
                </div>
                <div class="flex justify-center">
                    <img class="w-[70rem] absolute top-[43vh] z-[2]" src="~/assets/images/elements/table.png"
                        alt="man zittend aan tafel">
                </div>
            </div>
            <section class="hero2 panel text-black bg-blue">
                <h1>Horizontal snapping sections (simple)</h1>
                <p>Scroll vertically to scrub the horizontal animation. It also dynamically snaps to the sections in
                    an organic way based on the velocity. The snapping occurs based on the natural ending position
                    after momentum is applied, not a simplistic "wherever it is when the user stops".</p>
            </section>
            <section class="hero3 panel text-black ">
                <h1>Horizontal snapping sections (simple)</h1>
            </section>
        </div>
    </div>
</template>

<script setup>

import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { onMounted } from 'vue'


onMounted(() => {
    gsap.registerPlugin(ScrollTrigger);

    let sections = gsap.utils.toArray(".panel");
    gsap.to(sections, {
        xPercent: -100 * (sections.length - 1),
        ease: "none",
        scrollTrigger: {
            trigger: ".container1",
            pin: true,
            scrub: 1,
            snap: 1 / (sections.length - 1),
            // base vertical scrolling on how wide the container is so it feels more natural.
            end: "+=4000",
        }
    });
})





</script>

<style scoped>
body {
    overscroll-behavior: none;
    height: 100vh;
}

.container1 {
    overscroll-behavior: none;
    width: 300%;
    height: 100vh;
    display: flex;
    flex-wrap: nowrap;
}

.hero1 {
    background: url(~/assets/images/background/sea.png);
    height: 100vh;
    width: 100%;
    background-size: cover;
    background-position: bottom;
}

.hero2 {
    background: url(~/assets/images/background/sea.png);
    height: 100vh;
    width: 100%;
    background-size: cover;
    background-position: bottom;
}

.hero3 {
    background: url(~/assets/images/background/sea.png);
    height: 100vh;
    width: 100%;
    background-size: cover;
    background-position: bottom;
}
</style>