<template lang="html">
    <div class="slides">
        <img
            :class="{
                'slide-img': true,
                currentSlide: slide == index,
                'right-1': slide == mod(index + 1, 7),
                'left-1': slide == mod(index - 1, 7),
                'right-2': slide == mod(index + 2, 7),
                'left-2': slide == mod(index - 2, 7),
                'right-3': slide == mod(index + 3, 7),
                'left-3': slide == mod(index - 3, 7)}"
            :id="'slide'+slide"
            v-for="slide in slides"
            :src="imageLink + 'slide' + slide + '.jpg'"
        >
    </div>
</template>

<script>
export default {
    props: ['index', 'imageLink', 'slides', 'mod'],
}
</script>

<style lang="scss">
</style>
