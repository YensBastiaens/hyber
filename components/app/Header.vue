<script setup>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { onMounted } from 'vue'

onMounted(() => {
    gsap.registerPlugin(ScrollTrigger);

    gsap.fromTo('.navigation',
        {
            background: 'linear-gradient(360deg, rgba(0,0,0,0) 0%, rgba(0,0,0,0) 100%)'
        },
        {
            background: 'linear-gradient(360deg, rgba(0,0,0,0) 0%, rgba(0,0,0,1) 100%)',
            paddingBottom: '2rem',
            scrollTrigger: {
                trigger: '.trigger1',
                start: 'top 80%',
            }
        }
    )
});
</script>

<template>
    <section class="navigation flex justify-center fixed w-full z-[40] ">
        <nav class="container flex flex-row justify-between items-center pt-[3.5rem] ">
            <a href="#"><img href="#" class="flex items-center w-[18rem] h-[4.5rem]"
                    src="~/assets/images/logo/logoWhite.svg" alt="logo"></a>

            <div class="flex gap-[2.5rem] font-bold text-white">
                <a href="#">Werkgever HQ</a>
                <a href="#">Werknemerskwartier</a>
                <a href="#">Productiehal</a>
                <a href="#">Receptie</a>
            </div>
        </nav>
    </section>

</template>

<style scoped>
</style>