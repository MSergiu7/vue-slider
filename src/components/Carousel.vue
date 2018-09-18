<template lang="html">
    <div class="carousel">
        <app-slide :index="index" :slides="slides" :imageLink="imageLink" :mod="mod"></app-slide>
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
            index: 0,
            slides: [0, 1, 2, 3, 4, 5, 6]
        }
    },
    methods: {
        mod(a, b) {
        	var m = (( a % b) + b) % b;
        	return m < 0 ? m + Math.abs(b) : m;
        },
        nextSlide() {
            if (this.index == 6) {
                this.index = 0;
            } else {
                this.index++;
            }
            console.log('Index', this.index);
        },
        prevSlide() {
            if (this.index == 0) {
                this.index = 6;
            } else {
                this.index--;
            }
            console.log('Index', this.index);
        }
    }
}
</script>

<style lang="scss">
</style>
