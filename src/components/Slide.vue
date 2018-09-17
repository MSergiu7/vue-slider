<template lang="html">
    <div class="slides">
        <img
            :class="{
                'slide-img': true,
                currentSlide: slide == index,
                'right-1': slide == index + 1,
                'left-1': slide == index - 1,
                'left-2': slide == index - 2,
                'right-2': slide == index + 2,
                'left-3': slide == index - 3,
                'right-3': slide == index + 3}"
            :id="'slide'+slide"
            v-for="slide in slides"
            :src="imageLink + 'slide' + slide + '.jpg'">
    </div>
</template>

<script>
export default {
    props: ['index', 'imageLink', 'slides'],
}
</script>

<style lang="sass">
</style>
