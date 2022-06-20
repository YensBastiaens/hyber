<script setup>

const date1 = new Date();
const timeLondon = date1.toLocaleTimeString('nl-BE', { timeZone: 'Europe/London', hour: '2-digit', minute: '2-digit'})
const timeTokyo = date1.toLocaleTimeString('nl-BE', { timeZone: 'Asia/Tokyo', hour: '2-digit', minute: '2-digit'})
const timeAntarctica = date1.toLocaleTimeString('nl-BE', { timeZone: 'Antarctica/South_Pole', hour: '2-digit', minute: '2-digit'})

</script>

<template>
    <section>
        <div class="hero">
            <div class="layer"></div>
            <div class="container relative z-10 flex justify-center">
                <div class="flex flex-col">
                    <h1 class="text-white pt-[24vh]">Run je HQ vanuit...</h1>
                    <div class="flex justify-center gap-[2rem] text-white  mt-[6rem]">
                        <div class="hoverTime flex flex-col items-center p-[66px_55px]">
                            <div class="label">London</div>
                            <h4 >{{ timeLondon}} </h4>
                        </div>
                        <div class="hoverTime flex flex-col items-center p-[66px_55px]">
                            <div class="label">Tokyo</div>
                            <h4>{{timeTokyo}}</h4>
                        </div>
                        <div class="hoverTime flex flex-col items-center p-[66px_55px]">
                            <div class="label">Antartica</div>
                            <h4 >{{ timeAntarctica }} </h4>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style  scoped>

.hoverTime:hover {
    background: rgba(255, 255, 255, 0.2);
    border: 1px solid rgba(255, 255, 255, 0.4);
    backdrop-filter: blur(5px);
    border-radius: 20px;
    cursor: pointer;
}

.hoverTime {
    border: 1px solid rgb(255, 255, 255, 0.0);
}

.hero {
    background-image: url(~/assets/images/background/group.png);
    background-size: cover;
    position: relative;
    background-position: bottom;
    height: 100vh;
    width: 100%;
    backdrop-filter: blur(5px);
}

.layer {
    background: linear-gradient(135deg, #031A27 0%, #06131A 100%);
    opacity: 0.3;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 0;
}
</style>