<script>
export default {
    name: 'SectionNewmovie2',
    data() {
        return {
            section: [
                {
                    title: 'New Movie',
                    subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesettin'
                }
            ],
            genres: ['All', 'Coming Soon', 'Latest Movie', 'Top Rating', 'Tv Series'],
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
                    title: "Animate Blue Strack New Movie",
                    img: "src/assets/img/5 (1).jpg",
                    category: "Latest Movie",
                    details: "Details",
                    views: "343 Views",
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
                    title: "Nulla Strack New Animate Movie",
                    img: "src/assets/img/4.jpg",
                    category: "Tv Series",
                    details: "Details",
                    views: "324 Views",
                    star: "0/10"
                },
                {
                    title: "Quisque In Strack New Movie",
                    img: "src/assets/img/3 (1).jpg",
                    category: "Top Rating",
                    details: "Details",
                    views: "339 Views",
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
            ]
        }
    }
};
</script>
<template>
    <section id="new-movie-2">
        <!-- Container -->
        <div class="container pt-5">
            <!-- Section title -->
            <div class="pb-2 ps-3 section-title text-white d-flex justify-content-between align-items-center">
                <div>
                    <h2>{{ section[0].title }}</h2>
                    <span>{{ section[0].subtitle }}</span>
                </div>
            </div>
            <!-- Genre movies list  -->
            <div class="py-4">
                <ul class="d-flex">
                    <!-- for cycle on genres arrays -->
                    <li class="fs-5 pe-4" v-for="(genre, index) in genres" :key="genre"
                        :class="{ 'text-colored': index === 0 }">{{ genre }}
                    </li>
                </ul>
            </div>
            <!-- Row with cards -->
            <div class="row g-4">
                <!-- for cycle on movies object array -->
                <div class="col-4" v-for="movie in movies" :key="movie.title">
                    <!-- Card -->
                    <div class="card-custom">
                        <!-- card img -->
                        <img :src="movie.img" class="card-image">
                        <!-- card body -->
                        <div class="card-body">
                            <h3 class="card-title fw-bold">{{ movie.title }}</h3>
                            <span class="card-category fw-bold fs-5">Category: {{ movie.category }}</span>
                            <span class="card-details">{{ movie.details }}</span>
                            <span class="card-views">{{ movie.views }}</span>
                            <span class="card-star">
                                <i class="fa-solid fa-star text-colored pe-1"></i>{{ movie.star }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

// Section new movie 2
#new-movie-2 {
    min-height: 500px;
    background-color: $dark-blue;

    .section-title {
        border-bottom: 1px solid $light-blue;
        border-left: 2px solid $primary;
    }

    // Generics
    li {
        color: $white;
        cursor: pointer;
    }

    .text-colored {
        color: $primary;
    }

    // Card
    .card-custom {
        position: relative;
        color: $white;
    }

    .card-image {
        height: 500px;
        width: 100%;
        filter: brightness(0.6);
    }

    // Card body
    .card-title {
        position: absolute;
        bottom: 125px;
        left: 12px;
    }

    .card-category {
        position: absolute;
        bottom: 90px;
        left: 12px;
    }

    .card-views {
        position: absolute;
        bottom: 25px;
        right: 0;
        padding: 4px 12px;
        background-color: $dark-blue;
        border-top-left-radius: 18px;
        border-bottom-left-radius: 18px;
    }

    .card-details {
        position: absolute;
        bottom: 25px;
        left: 0;
        padding: 4px 12px;
        background-color: $dark-blue;
        border-top-right-radius: 18px;
        border-bottom-right-radius: 18px;
    }

    .card-star {
        position: absolute;
        top: 20px;
        right: 10px;
    }

}
</style>