<script setup>

</script>

<template>
    <section class="relative" id="answer">
        <img class="absolute right-[0] top-[-15rem]" src="~/assets/images/elements/parrot.png" alt="papegaai">
        <div class="container relative py-[18rem] pb-[25rem]">
             
            <div class="flex justify-between ">
                <div class="">
                    <h3>Ik ben<br>een werkgever</h3>
                    <p class="max-w-[40.9rem] pt-[3.5rem]">Je workforce volledig remote laten werken mét behoud van
                        controle en efficiëntie? Het kan zomaar. Meer nog, Hyber helpt je operational excellence met
                        rasse schreden vooruit.</p>
                    <BtnBlackButton :href="'#'" :text="'Hyber voor werkgevers'" />
                    <img class="origami absolute bottom-[-29rem] left-[13rem] right-[50rem]"
                        src="~/assets/images/elements/origami.png" alt="origami">
                </div>
                <img class="dottedLine" src="~/assets/images/elements/dottedLineText.png" alt="origami">
                <div class="mt-[20.3rem]">
                    <h3>Ik ben<br>een werknemer</h3>
                    <p class="max-w-[40.9rem] pt-[3.5rem]">De ideale work/life balance is dichterbij dan je denkt.
                        Dankzij Hyber plan jij je werkdag in zoals jij het wil. Je collega’s? Die zijn slechts een klik
                        verwijderd. Never alone, always together. </p>
                    <BtnBlackButton :href="'#'" :text="'Hyber voor werknemers'"/>
                </div>
            </div>
        </div>
    </section>
</template>


<style  scoped>

section {
    background: linear-gradient(90deg, #88FFF0 50%, #A9F58D 50%);
    height: 100%;
}

.origami {
    transform: translateX(-25%);
}

.dottedLine {
    position: absolute;
    margin-left: auto;
    margin-right: auto;
    top: 16%;
    left: -5%;
    right: 0;
    text-align: center;
}


</style>