<template lang="html">
    <div class="carousel">
        <app-slide :index="index" :slides="slides" :imageLink="imageLink"></app-slide>
        <div class="navigation">
            <i class="fas fa-chevron-left" @click="prevSlide"></i>
            <i class="fas fa-chevron-right" @click="nextSlide"></i>
        </div>
    </div>
</template>

<script>
import Slide from './Slide.vue'

export default {
    components: {
        'appSlide': Slide
    },
    data() {
        return {
            imageLink: './img/',
            index: 1,
            slides: 7
        }
    },
    methods: {
        nextSlide() {
            if (this.index == 7) {
                this.index = 1;
            } else {
                this.index++;
            }
            console.log('Index', this.index);
        },
        prevSlide() {
            if (this.index == 1) {
                this.index = 7;
            } else {
                this.index--;
            }
            console.log('Index', this.index);
        }
    }
}
</script>

<style lang="sass">
</style>
