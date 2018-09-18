<template lang="html">
    <div class="carousel">
        <app-slide :index="index" :slides="slides" :imageLink="imageLink"></app-slide>
        <div class="navigation">
            <i class="fas fa-chevron-left" @click="prevSlide"></i>
            <i class="fas fa-chevron-right" @click="nextSlide"></i>
        </div>
        <p>Index: {{index}} Slide: {{ (-2)%7 }}</p>
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
            index: 3,
            slides: [0, 1, 2, 3, 4, 5, 6]
        }
    },
    methods: {
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

<style lang="sass">
</style>
