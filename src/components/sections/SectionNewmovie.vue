<script>
import NewmoviesCard from '../cards/NewmoviesCard.vue';
export default {
    name: 'SectionNewmovie',
    components: { NewmoviesCard },
    data() {
        return {
            currentIndex: 0,
            section: [
                {
                    title: 'New Movie',
                    subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesettin'
                }
            ],
            movies: [
                {
                    title: "Hurry Animate Blue Strack New Movie",
                    img: "src/assets/img/1.jpg",
                    category: "Top rating",
                    details: "Details",
                    views: "381 Views",
                    star: "0/10"
                },
                {
                    title: "Quisque Auctor Movie in Strack",
                    img: "src/assets/img/2.jpg",
                    category: "Coming Soon",
                    details: "Details",
                    views: "947 Views",
                    star: "4/10"
                },
                {
                    title: "New Movie Quisque In Strackk",
                    img: "src/assets/img/5.jpg",
                    category: "Latest Movie",
                    details: "Details",
                    views: "721 Views",
                    star: "0/10"
                },
                {
                    title: "Movie Action Garila English",
                    img: "src/assets/img/3.jpg",
                    category: "Top Rating",
                    details: "Details",
                    views: "365 Views",
                    star: "1/10"
                },
                {
                    title: "Action Garila English Movie",
                    img: "src/assets/img/3-1.jpg",
                    category: "TV Series",
                    details: "Details",
                    views: "296 Views",
                    star: "0/10"
                },
                {
                    title: "Donec English Action Movies",
                    img: "src/assets/img/2-1 (1).jpg",
                    category: "Coming Soon",
                    details: "Details",
                    views: "481 Views",
                    star: "10/10"
                },
                {
                    title: "English Action Movie In Strack",
                    img: "src/assets/img/4-1.jpg",
                    category: "Latest Movie",
                    details: "Details",
                    views: "277 Views",
                    star: "0/10"
                },
                {
                    title: "Movie Auctor Quisque In Strack",
                    img: "src/assets/img/6.jpg",
                    category: "Top Rating",
                    details: "Details",
                    views: "300 Views",
                    star: "0/10"
                },
                {
                    title: "Auctor Movie Quisque In Strack",
                    img: "src/assets/img/5-1.jpg",
                    category: "Tv Series",
                    details: "Details",
                    views: "343 Views",
                    star: "1/10"
                },
                {
                    title: "Donec Movie Quisque In Strack",
                    img: "src/assets/img/1-2.jpg",
                    category: "Coming Soon",
                    details: "Details",
                    views: "361 Views",
                    star: "1/10"
                },
                {
                    title: "New Movie Quisque In Strack",
                    img: "src/assets/img/2-1.jpg",
                    category: "Latest Movie",
                    details: "Details",
                    views: "503 Views",
                    star: "0/10"
                },
                {
                    title: "Quisque In Strack New Movie",
                    img: "src/assets/img/3 (1).jpg",
                    category: "Top Rating",
                    details: "Details",
                    views: "341 Views",
                    star: "1/10"
                },
                {
                    title: "Nulla Strack New Animate Movie",
                    img: "src/assets/img/4.jpg",
                    category: "Tv Series",
                    details: "Details",
                    views: "326 Views",
                    star: "0/10"
                },
                {
                    title: "Blue Strack New Animate Movie",
                    img: "src/assets/img/3.jpg",
                    category: "Coming Soon",
                    details: "Details",
                    views: "420 Views",
                    star: "0/10"
                },
                {
                    title: "Animate Blue Strack New Movie",
                    img: "src/assets/img/5 (1).jpg",
                    category: "Latest Movie",
                    details: "Details",
                    views: "346 Views",
                    star: "0/10"
                },
            ]
        }
    },
    computed: {
        // computed to take only three movies
        visibleMovies() {
            const slicedMovies = this.movies.slice(this.currentIndex, this.currentIndex + 3);
            if (slicedMovies.length === 2) {
                slicedMovies.push(this.movies[0]);
            }

            if (slicedMovies.length === 1) {
                slicedMovies.push(this.movies[0]);
                slicedMovies.push(this.movies[1]);
            }
            return slicedMovies;
        }
    },

    methods: {
        nextImage() {
            if (this.currentIndex === this.movies.length - 1) {
                this.currentIndex = 0;
            } else {
                this.currentIndex++;
            }
        },
        prevImage() {
            if (this.currentIndex === 0) {
                this.currentIndex = this.movies.length - 1;
            } else {
                this.currentIndex--;
            }
        }
    }
};
</script>
<template>
    <section id="new-movie">
        <!-- Container -->
        <div class="container pt-5">
            <!-- Section title with icons to change image  -->
            <div class="pb-2 ps-3 text-white section-title d-flex justify-content-between align-items-center">
                <div>
                    <h2>{{ section[0].title }}</h2>
                    <span>{{ section[0].subtitle }}</span>
                </div>
                <div>
                    <i class="fa-regular fa-circle-left fa-2x" @click="prevImage"></i>
                    <i class="fa-regular fa-circle-right fa-2x ps-2" @click="nextImage"></i>
                </div>
            </div>
            <!-- Row with for cycle and props passed to movies card -->
            <div class="row g-0 pt-4">
                <newmovies-card v-for="(movie, index) in visibleMovies" :key="index" :movie="movie"></newmovies-card>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

// Section
#new-movie {
    min-height: 500px;
    background-color: $dark-blue;
    margin-top: 520px;

    .section-title {
        border-bottom: 1px solid $light-blue;
        border-left: 2px solid $primary;

        // Class icons
        .fa-regular {
            color: $primary;
            cursor: pointer;

            &:hover {
                color: $white;
            }
        }
    }


}
</style>