<script>
export default {
    name: 'SectionLatestnews',
    data() {
        return {
            section: [
                {
                    title: 'Latest News',
                    subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesettin'
                }
            ],
            images: [
                {
                    title: "Actor The Concept Movie High Concept Theory See The Post",
                    img: "src/assets/img/blog-570x570.jpg",
                    author: "moviestar",
                    details: "Details",
                    comments: "0 Comment",
                    share: "Share"
                },
            ],
            thumbnails: [
                {
                    title: "Consequat Nam Lectus Nibh Aucibus It Has Turpis",
                    img: "src/assets/img/blog2-300x300.jpg",
                    details: "Details",
                    share: "Share"
                },
                {
                    title: "Nam Lectus Nibh Consequat Aucibus Turpis It Has",
                    img: "src/assets/img/blog3-300x300.jpg",
                    details: "Details",
                    share: "Share"
                },
                {
                    title: "Bring Me The Head Of Alfredo Garcia Best Movie In",
                    img: "src/assets/img/blog4-300x300.jpg",
                    details: "Details",
                    share: "Share"
                },
                {
                    title: "Pump Action Interaction English Action Movie (2020",
                    img: "src/assets/img/blog5-300x300.jpg",
                    details: "Details",
                    share: "Share"
                }
            ]
        }
    }
};
</script>

<template>
    <section id="latest-news">
        <!-- Container -->
        <div class="container py-5">
            <!-- Section title -->
            <div class="pb-2 ps-3 section-title text-white d-flex justify-content-between align-items-center">
                <div>
                    <h2>{{ section[0].title }}</h2>
                    <span>{{ section[0].subtitle }}</span>
                </div>
            </div>
            <!-- Row with cards -->
            <div class="row pt-4">
                <!-- Single big card on left -->
                <div class="col-6">
                    <div class="card-custom">
                        <img :src="images[0].img" class="card-image">
                        <div class="card-body">
                            <h3 class="card-title fw-bold">{{ images[0].title }}</h3>
                            <span class="card-details">{{ images[0].details }}</span>
                            <div class="card-info">
                                <span class="card-author">{{ images[0].author }}</span>
                                <span class="card-comments ps-3">{{ images[0].comments }}</span>
                                <span class="card-share ps-3">{{ images[0].share }}</span>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Four cards small on right -->
                <div class="col-6">
                    <!-- Row inside col for bootstrap -->
                    <div class="row h-100 gy-2">
                        <!-- For cycle single thumbnails -->
                        <div class="thumbnails h-50 w-50" v-for="thumbnail in thumbnails" :key="thumbnail.title">
                            <div class="thumbnails-custom">
                                <img :src="thumbnail.img" class="thumbnails-image">
                                <div class="thumnails-body">
                                    <h5 class="thumbnails-title fw-bold">{{ thumbnail.title }}</h5>
                                    <span class="thumbnails-details">{{ thumbnail.details }}</span>
                                    <span class="thumbnails-share ps-3">{{ thumbnail.share }}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

// Section latest news
#latest-news {
    min-height: 500px;
    background-color: $dark-blue;

    .section-title {
        border-bottom: 1px solid $light-blue;
        border-left: 2px solid $primary;
    }

    // Generics for cols
    .col-6 {
        min-height: 520px;

        .card-custom,
        .thumbnails-custom {
            color: $white;
            position: relative;

            .card-image,
            .thumbnails-image {
                height: 100%;
                width: 100%;
                filter: brightness(0.4);
            }

            .card-details,
            .thumbnails-details {
                position: absolute;
                bottom: 25px;
                left: 0;
                padding: 4px 12px;
                background-color: $dark-blue;
                border-top-right-radius: 18px;
                border-bottom-right-radius: 18px;
            }

            // Single big card on left
            .card-title {
                position: absolute;
                bottom: 90px;
                padding: 4px 12px;
            }

            .card-info {
                position: absolute;
                bottom: 25px;
                right: 15px;
                padding: 4px 12px;
            }


            // Four cards small on right - thumbnails
            .thumbnails-title {
                position: absolute;
                bottom: 70px;
                padding: 4px 12px;
            }

            .thumbnails-share {
                position: absolute;
                bottom: 25px;
                padding: 4px 12px;
                right: 18px;
            }
        }
    }
}
</style>