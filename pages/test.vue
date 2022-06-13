<template>
    <section>
        <div class="container1">
            <section class="hero panel bg-red-400">

                <div class="container flex justify-center">
                    <h1 class="pt-[15vh] text-white text-center  absolute z-[2] ">Met hyber werk <br> je van overal</h1>
                </div>
                <div class="flex justify-center">
                    <img class="w-[70rem] absolute top-[43vh] z-[2]" src="~/assets/images/elements/table.png"
                        alt="man aan tafel">
                </div>
                <div class="blur"></div>
            </section>

            <section class="hero panel text-black bg-blue">
                <h1>Horizontal snapping sections (simple)</h1>
                <p>Scroll vertically to scrub the horizontal animation. It also dynamically snaps to the sections in
                    an organic way based on the velocity. The snapping occurs based on the natural ending position
                    after momentum is applied, not a simplistic "wherever it is when the user stops".</p>
            </section>

            <section class="hero">
                <img class="right-[58vh] top-[14.5vh] absolute z-[2]" src="~/assets/images/elements/fish.png" alt="vis">
                <div class="flex justify-center">
                    <h1 class="pt-[15vh] text-white text-center  absolute z-[1] ">Nee, serieus. <br>Echt overal.</h1>
                </div>
                <div class="flex justify-center">
                    <img class="w-[70rem] absolute top-[43vh] z-[2]" src="~/assets/images/elements/table.png"
                        alt="man aan tafel">
                </div>
                <div class="blur"></div>
            </section>
        </div>
    </section>
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
.container1 {
    width: 300%;
    height: 100vh;
    display: flex;
}

.hero {
    height: 100vh;
    width: 100%;
}

.blur {
    background: url(~/assets/images/background/savannah.png);
    filter: blur(2px);
    height: 100vh;
    width: 100%;
    background-size: cover;
    position: absolute;
    background-position: 0% 20%;
}
</style>