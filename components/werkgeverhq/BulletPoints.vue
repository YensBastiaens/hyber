<script setup>


</script>
<template>
    <section class="backgroundGradient relative" id="answer">
        <div class="planets"></div>
        <div class="container relative py-[10rem]">
            <div class="flex justify-between items-center relative z-[3]">
                <h4 class="text-white ">Alles werkt beter met Hyber<span class="text-blue">.</span></h4>
                <BtnBlueButton :text="'Ontdekken'" />
            </div>
            <div class="flex justify-end mt-[13rem]">
                <div class="flex flex-col">
                    <div class="flex flex-col relative max-h-[17rem] max-w-[50rem] py-[5rem]">
                        <div class="stipellijn"></div>
                        <div class="flex gap-[1.5rem] items-center">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">Say it with Hyber</div>
                        </div>
                        <p class="text-white max-w-[43.3rem] ml-[2.8rem] mt-[1rem]">Moppen tappen aan de waterkoeler is
                            zó
                            1999. Vandaag stuur je toch een GIF via chat om je medewerkers aan het lachen te krijgen?
                            Best handig, die instant communciatie.</p>
                    </div>
                    <div class="flex flex-col relative max-h-[17rem] max-w-[50rem] py-[5rem]">
                        <div class="stipellijn"></div>
                        <div class="flex gap-[1.5rem] items-center relative z-[3]">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">See it with Hyber</div>
                        </div>
                        <p class="text-white max-w-[43.3rem] ml-[2.8rem] mt-[1rem]">Hyber brengt je hele organisatie
                            samen
                            op 1 digitale stek. Zo weet je meteen welke collega een griepje heeft, welke klant je best
                            opbelt en welke partner je nog moet trakteren.</p>
                    </div>
                    <div class="flex flex-col relative max-h-[17rem] max-w-[50rem] py-[5rem]">
                        <div class="stipellijn"></div>
                        <div class="flex gap-[1.5rem] items-center relative z-[3]">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">Secure it with Hyber</div>
                        </div>
                        <p class="text-white  max-w-[43.3rem] ml-[2.8rem] mt-[1rem]">In een digitale wereld horen
                            privacy
                            en security hand in hand te gaan. Hyber cyberverzegelt al je documenten, bestanden en
                            gesprekken op een veilige manier. #safespace</p>
                    </div>
                    <div class="flex flex-col relative max-h-[17rem] max-w-[50rem] py-[5rem]">
                        <div class="stipellijn"></div>
                        <div class="flex gap-[1.5rem] items-center relative z-[3]">
                            <img class="h-[1.8rem]" src="~/assets/images/logo/smallLogoIcon.png" alt="logo">
                            <div class="title text-white">Speed it up with Hyber</div>
                        </div>
                        <p class="text-white max-w-[43.3rem] ml-[2.8rem] mt-[1rem]">Wij garanderen dat jouw digitale
                            werkomgeving up and running is binnen de twee(!) weken. Dat digitale meerjarenplan dat je
                            voor ogen had? Verticaal klasseren.</p>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>



<style scoped>
.bottomGradient {
    background: linear-gradient(180deg, rgba(6, 19, 26, 0) 0%, #06131A 100%);
    position: absolute;
    z-index: 5;
    bottom: 98rem;
    width: 100%;
    height: 23rem;
    transform: matrix(-1, 0, 0, 1, 0, 0);
}

.stipellijn {
    width: 74.6rem;
    border-top: 2px dashed rgba(255, 255, 255, 0.3);
    transform: rotate(-180deg);
    position: absolute;
    left: -80rem;
    top: 6rem;

}

.planets {
    background: url(~/assets/images/elements/planets.png);
    width: 1195px;
    height: 783px;
    position: absolute;
    top: 31rem;
    z-index: 2;

    background-repeat: no-repeat;


}

.backgroundGradient {
    background: rgb(6, 19, 26);
    margin-top: -1rem;
}
</style>