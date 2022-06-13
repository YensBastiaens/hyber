<script setup>
const props = defineProps({
    text: String,
    url: String,
});
</script>

<template>

    <a class="
    label
      relative
       text-blue
      cursor-pointer
      top-[26rem]
      left-[2.5%]
      flex
      justify-center
      z-50
    " :href="url">
        <div class="dottedLine"></div>
        <div class="flex gap-[2.7rem] ">
            <SvgArrow class=" button w-[18px] h-[12px] fill-current text-blue" />
            {{ text }}
        </div>

    </a>
</template>

<style scoped>
.dottedLine {
    background: url(~/assets/images/elements/dottedLine.png);
    transform: rotate(90deg);
    height: 290px;
    width: 3px;
    position: absolute;
    bottom: -11rem;
}

.label {
    transform: rotate(-90deg);
}
</style>