<template>
    <footer class="footerBackground">
        <div class="container">
            <div class="flex justify-between">
                <div class="flex flex-col">
                    <img src="~/assets/images/logo/logoWhite.svg" alt="logo">
                    <div class="flex flex-row gap-[2.2rem] pt-[3.1rem]">
                        <a href="#"><img src="~/assets/images/icons/facebookBlue.svg" alt="Facebook"></a>
                        <a href="#"><img src="~/assets/images/icons/twitterBlue.svg" alt="Twitter"></a>
                        <a href="#"><img src="~/assets/images/icons/instagramBlue.svg" alt="Instagram"></a>
                    </div>
                </div>
                <div>
                    <nav class="container flex flex-col text-white gap-[1rem] pt-[1rem] ">
                        <a href="#">Productiehal</a>
                        <a href="#">Receptie</a>
                        <a href="#">Werkgever HQ</a>
                        <a href="#">Werknemerskwartier</a>
                    </nav>
                </div>
            </div>
            <div class="copyright"></div>
            <div class=" flex justify-between leading-[1.4rem] text-[1.2rem] items-center pb-[1.8rem] pt-[2.6rem]">
                <p class="text-white uppercase">© Hyber 2022. Alle rechten voorbehouden.</p>
                <div class="flex uppercase text-white gap-[1.5rem]">
                    <a href="#">Disclaimer</a>
                    <a href="#">Privacy policy</a>
                    <a href="#">Cookie policy</a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>

</script>

<style scoped>
.footerBackground {
    background: linear-gradient(314.34deg, #06131B 100%, #1E3D39 100%);
}

.copyright {
    border: 1px dashed rgba(255, 255, 255, 0.1);
    transform: rotate(180deg);
    margin-top: 4rem;
}
</style>