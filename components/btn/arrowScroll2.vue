<script setup>
const props = defineProps({
    text: String,
    url: String,
});
</script>

<template>

    <a class="
    scroll-down
    label
      relative
       text-blue
      cursor-pointer
      top-[18rem]
      left-[1%]
      flex
      justify-center
      z-50
    " :href="url">
        <div class="dottedLine"></div>
        <div class="flex gap-[2.7rem] ">
            <SvgArrow class=" button w-[18px] h-[12px] fill-current text-blue" />
            {{ props.text }}
        </div>

    </a>
</template>

<style scoped>
html {
    scroll-behavior: smooth;
}

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