<script>
export default {
    name: 'JumbotronHeader',
    data() {
        return {
            currentSlideIndex: 0,
            slides: [
                {
                    img: 'src/assets/img/slider-1536x520.jpg',
                    welcome: 'Welcome To Our Movies Site',
                    h2: 'OUR SPECIAL MOVIES',
                    h2Colored: 'MOVIES',
                    paragraph: 'Lorem Ipsum is Simply dummy text of the printing and typesetting industrioy. Lorem Ipsum has been the industry standard dummy text ever since the 1500s, when an unknown',
                    button: 'Read More'
                },
                {
                    img: 'src/assets/img/slider-2-1536x520.jpg',
                    welcome: 'Bienvenue Sur Notre Site De Films',
                    h2: 'NOS FILMS SPÉCIAUX',
                    h2Colored: 'FILMS',
                    paragraph: 'Lorem Ipsum est tout simplement un texte factice utilisé dans l\'industrie de l\'impression et de la mise en page. Lorem Ipsum a été le texte factice standard de l\'industrie depuis les années 1500, lorsqu\'un inconnu',
                    button: 'En savoir plus'
                },
            ],
        }
    },
    computed: {
        currentSlide() {
            return this.slides[this.currentSlideIndex];
        }
    },
    methods: {
        previousSlide() {
            this.currentSlideIndex--;
            if (this.currentSlideIndex < 0) {
                this.currentSlideIndex = this.slides.length - 1;
            }
        },
        nextSlide() {
            this.currentSlideIndex++;
            if (this.currentSlideIndex >= this.slides.length) {
                this.currentSlideIndex = 0;
            }
        },
    }
}

</script>
<template>
    <div class="jumbotron-header">
        <!-- Arrow prev -->
        <i class="fa-solid fa-arrow-left fa-2x ps-5" @click="previousSlide"></i>
        <!-- Jumbotron content -->
        <div class="jumbotron-header-content text-white" :style="{ backgroundImage: `url(${currentSlide.img})` }">
            <span>{{ currentSlide.welcome }}</span>
            <h2>{{ currentSlide.h2 }} <span class="title-colored">{{ currentSlide.h2Colored }}</span></h2>
            <p class="paragraph-jumbotron text-center">{{ currentSlide.paragraph }}</p>
            <button class="text-white border-0 rounded-5 px-4 py-2">{{ currentSlide.button }}</button>
        </div>
        <!-- Arrow next -->
        <i class="fa-solid fa-arrow-right fa-2x pe-5" @click="nextSlide"></i>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.jumbotron-header {
    height: 520px;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;

    // Arrows
    .fa-solid {
        position: absolute;
        top: 50%;
        transform: translate(0, -50%);
        color: $white;
        cursor: pointer;

        &:hover {
            color: $primary;
        }
    }

    .fa-arrow-right {
        right: 0;
    }

    // Jumbotron content
    .jumbotron-header-content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
        padding-left: 300px;
        transition: background-image 1s;

        .title-colored {
            color: $primary;
        }

        .paragraph-jumbotron {
            width: 40%;
        }

        button {
            background-color: $primary;
        }
    }
}
</style>