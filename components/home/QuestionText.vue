<script setup>

</script>

<template>
    <section class="backgroundGradient ">
        <div class="relative">
        <div class="container py-[29rem]">
            <div class="flex justify-center">
            <div class="max-w-[101rem]">
                <h2 class="text-white text-center">Wacht? Hoe werkt dat dan?</h2>
                <div class="flex gap-[1rem] justify-end items-center  ">
                    <p class="title text-white text-right">(Het is heel simpel eigenlijk)</p>
                    <img src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                </div>
                <div class="flex justify-center">
                    <p class="text-white text-center max-w-[66rem] mt-[6rem]">Bye bye papierwerk, hallo digitale
                        vrijheid! Met Hyber
                        werk jij waar en wanneer je wil. Net zoals de rest
                        van je workforce! Hier mag nog een extra zinnetje of twee uitleg bij komen over wat Hyber
                        precies
                        is.
                    </p>
                </div>
                <div class="logo"></div>
                <div class="">
                    <BtnArrowScroll :text="'Wat betekent dat voor mij?'" />
                </div>
            </div>
            </div>
        </div>
        </div>
    </section>
</template>



<style  scoped>
.backgroundGradient {
    background: linear-gradient(314.34deg, #06131B 61.57%, #1E3D39 100%);
    padding-bottom: 35rem;
}

.logo {
    background: url(~/assets/images/logo/bigLogo.png);
    height: 74rem;
    width: 53rem;
    position: absolute;
    top: 11rem;
    left: -1rem;
    background-repeat: no-repeat;
}
</style>