<script setup>


import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { ref, onMounted } from 'vue'

const currentSection = ref('')

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
            snap: {
                snapTo: 1 / (sections.length - 1),
                inertia: false,
                duration: { min: 0.1, max: 0.1 }
            },
            toggleClass: { targets: sections, className: 'font-animation' },
            end: "+=1000",
        }
    });
    const observer = new IntersectionObserverEntry((entry) => {
        if (entry.intersectionRatio > 0) {
            currentSection.value = entry.target.getAttribute('id')
        }
    },
        {
            rootMargin: '0px 0px -90% 0px',
        }
    )

    document.querySelector('blurBackground3').forEach((section) => {
        observer.observe(section);
    });
})
</script>

<template>
    <section>
        <div class="container1 z-[30]">

            <div class="tafelman absolute justify-center z-[61] ">
                <img class="w-[70rem] relative top-[23vh]" src="~/assets/images/elements/table.png"
                    alt="man aan tafel">
            </div>
            
            <section class="hero panel z-[60]">
                <div class="blurBackground"></div>
                <div class="navGradientTop"></div>
                <img class="blur-[2px] left-[17vh] top-[42vh] absolute z-[2]"
                    src="~/assets/images/elements/elephant.png" alt="olifant">
                <div class="container flex justify-center z-[41] ">
                    <h1 class="pt-[15vh] text-white text-center  absolute z-[2]  ">Met hyber werk <br> je van overal
                    </h1>
                </div>
                <img class=" right-[0vh] top-[7vh] absolute z-[3] h-[62.4rem] w-[41.6rem]"
                    src="~/assets/images/elements/giraffe.png" alt="giraffe">

                <div class="navGradienBottom"></div>
            </section>

            <section class="hero panel z-[50]  ">
                <div class="blurBackground2"></div>
                <div class="navGradientTop"></div>
                <img class="left-[17vh] top-[12.5vh] absolute z-[2]" src="~/assets/images/elements/astronaut.png"
                    alt="astronaut">
                <div class="flex justify-center z-[50]">
                    <h1 class="pt-[15vh] text-white text-center  absolute z-[1] ">En dan bedoelen <br> we echt overal.
                    </h1>
                </div>
                <div class="flex justify-center">
                    <img class="w-[70rem] absolute top-[43vh] z-[2]" src="~/assets/images/elements/table.png"
                        alt="man aan tafel">
                </div>

                <div class="navGradienBottom"></div>
            </section>

            <section class="hero panel z-10 ">
                <div class="blurBackground3"></div>
                <img class="right-[58vh] top-[14.5vh] absolute z-[2]" src="~/assets/images/elements/fish.png" alt="vis">
                <div class="flex justify-center">
                    <h1 class="pt-[15vh] text-white text-center  absolute z-[1] ">Nee, serieus. <br>Echt overal.</h1>
                </div>
                <div class="flex justify-center">
                    <img class="w-[70rem] absolute top-[43vh] z-[2]" src="~/assets/images/elements/table.png"
                        alt="man aan tafel">
                </div>

                <div class="navGradienBottom"></div>
            </section>

        </div>
    </section>
</template>

<style scoped>

.navGradientTop {
    background: linear-gradient(180deg, rgba(6, 19, 26, 0.6) 0%, rgba(6, 19, 26, 0) 100%);
    width: 100%;
    height: 35rem;
    position: absolute;
}

.container1 {
    width: 300%;
    display: flex;
    align-content: center;
    align-items: center;
}

.hero {
    height: 100vh;
    width: 100%;
}

.blurBackground {
    background: url(~/assets/images/background/savannah.png);
    filter: blur(2px);
    height: 100vh;
    width: 100%;
    background-size: cover;
    position: absolute;
    background-position: 0% 20%;
}

.blurBackground2 {
    background: url(~/assets/images/background/space.png);
    filter: blur(2px);
    height: 100vh;
    width: 100%;
    background-size: cover;
    position: absolute;
    background-position: 0% 30%;
}

.blurBackground3 {
    background: url(~/assets/images/background/sea.png);
    filter: blur(2px);
    height: 100vh;
    width: 100%;
    background-size: cover;
    position: absolute;
    background-position: bottom;
}

.navGradienBottom {
    position: absolute;
    width: 100%;
    height: 30rem;
    bottom: -14.5rem;
    background: linear-gradient(180deg, rgba(6, 19, 26, 0) 0%, #06131A 51.3%, rgba(6, 19, 27, 0) 100%);
    transform: matrix(-1, 0, 0, 1, 0, 0);
}
</style>