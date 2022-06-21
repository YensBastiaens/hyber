<script setup>
import { reactive } from 'vue';

function scroll() {
    document.getElementById('answer')?.scrollIntoView({ behavior: 'smooth' })
}

const images = reactive({
    fish: {
        src1: '~/assets/images/elements/fish2.png', src2: '~/assets/images/elements/fish3.png'
    },
    penguin: {
        src1: '~/assets/images/elements/penguin.png', src2: '~/assets/images/elements/penguin2.png'
    },
    owl: {
        src1: '~/assets/images/elements/owl.png', src2: '~/assets/images/elements/owl2.png'
    }
})

function changeImage1() {
    document.getElementById('fish1')
}
function changeImage2() {
    document.getElementById('fish2')
}
</script>

<template>
    <section class="backgroundGradient relative">
        <div class="gradientTop"></div>
        <div class="container pb-[60rem]">
            <div class="flex justify-center">
                <div class="grid grid-cols-2 relative gap-[2.5rem]">
                    <div
                        class="background flex flex-col justify-center rounded-[1rem] max-h-[17rem] max-w-[42rem] py-[5rem] px-[2.5rem] pr-[6rem] z-[1]">
                        <div class="flex gap-[1.5rem] items-center">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">Omnidigitaliteit</div>
                        </div>
                        <p class="text-white max-w-[31rem] ml-[2.8rem] mt-[1rem]">Hyber digitaliseert álles.
                            Klantenoffertes, HR-contracten, archiefdocumenten, boekhouding, en ja, ook wie welke topping
                            had gekozen bij pizza night.</p>
                    </div>
                    <div
                        class="background relative flex flex-col justify-center rounded-[1rem] max-h-[17rem] max-w-[42rem] py-[5rem] px-[2.5rem] pr-[6rem]">
                        <img src="~/assets/images/elements/fish3.png" alt="fish" class="absolute top-[-16rem] right-[-16rem] z-[2]">
                        <img src="src" id="fish1" alt="fish" class="absolute top-[-16rem] right-[-16rem] z-[2]">
                        <div class="flex gap-[1.5rem] items-center">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">Work/life war</div>
                        </div>
                        <p class="text-white max-w-[31rem] ml-[2.8rem] mt-[1rem]">De nieuwste generatie werknemers
                            verkiest een optimale work/life balance boven een hip kantoor of een vette loonbrief. Trek
                            het grootste talent aan met een hybride job.</p>
                    </div>
                    <div
                        class="background relative flex flex-col justify-center rounded-[1rem] max-h-[17rem] max-w-[42rem] py-[5rem] px-[2.5rem] pr-[6rem]">
                         <img src="~/assets/images/elements/fish2.png" alt="fish" class="absolute top-[35rem] left-[-14rem]">
                        <div class="flex gap-[1.5rem] items-center">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">Jij bent de baas</div>
                        </div>
                        <p class="text-white max-w-[31rem] ml-[2.8rem] mt-[1rem]">Behoud volledige controle over het
                            reilen en zeilen van je organisatie. Hyber logt werk- en productiviteitsdata zodat jij je
                            kan bezighouden met planning en organisatie.</p>

                    </div>
                    <div
                        class="background flex flex-col justify-center rounded-[1rem] max-h-[17rem] max-w-[42rem] py-[5rem] px-[2.5rem] pr-[6rem] z-[1]">
                        <div class="flex gap-[1.5rem] items-center">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">Lorem ipsum</div>
                        </div>
                        <p class="text-white max-w-[31rem] ml-[2.8rem] mt-[1rem]">Elk dossier en bestand is slechts een
                            vingerklik verwijderd. Zelf je agenda kunnen bepalen doet wonderen voor de productiviteit.
                            Suspendisse mattis</p>
                    </div>
                </div>
            </div>

            <div class="flex gap-[2.5rem] mt-[6rem] mb-[20rem]">
                <div class="w-[50%] flex justify-end">
                    <BtnBlueButton :text="'Demo aanvragen'" />
                </div>
                <div class="w-[50%] flex justify-start">
                    <BtnBlueButton class="current-fill bg-green" :text="'Naar de productiehal'" />
                </div>
            </div>
            <div class="flex justify-center gap-[2.5rem]">
            </div>
            <BtnArrowScroll2 :text="'ontdek meer coole features'" @click="scroll" />
        </div>

    </section>
</template>



<style scoped>
.gradientTop {
    background: linear-gradient(180deg, rgba(6, 19, 26, 0) 0%, #06131A 51.3%, rgba(6, 19, 27, 0) 100%);
    transform: matrix(-1, 0, 0, 1, 0, 0);
    height: 100px;
    width: 100%;
    position: absolute;
    margin-top: -5.3rem;
}

.backgroundGradient {
    background: rgb(6, 19, 26);
    margin-top: -1rem;
}

.background {
    background: rgba(54, 70, 79, 0.9);
    backdrop-filter: blur(5px);
    ;
}
</style>