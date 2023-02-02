<script>
export default {
    name: 'SectionMovieplaylist',
    data() {
        return {
            displayScreenDefault: 'd-block',
            displayScreenNew: 'd-none',
            section: [
                {
                    title: 'Movie Playlist',
                    subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesettin'
                }
            ],
            movies: [
                {
                    title: "Quisque Auctor Movie in Strack",
                    img: "src/assets/img/2.jpg",
                    date: "February 12,2016",
                    views: "956 Views",
                    number: "2.30.00"
                },
                {
                    title: "New Movie Quisque In Strackk",
                    img: "src/assets/img/5.jpg",
                    date: "February 12,2016",
                    views: "723 Views",
                    number: "2.30.00"
                },
                {
                    title: "Movie Action Garila English",
                    img: "src/assets/img/3.jpg",
                    date: "February 12,2016",
                    views: "366 Views",
                    number: "2.30.00"
                },
                {
                    title: "Action Garila English Movie",
                    img: "src/assets/img/3-1.jpg",
                    date: "February 12,2016",
                    views: "296 Views",
                    number: "2.30.00"
                },
                {
                    title: "Donec English Action Movies",
                    img: "src/assets/img/2-1 (1).jpg",
                    date: "February 12,2016",
                    views: "481 Views",
                    number: "2.30.00"
                },
                {
                    title: "English Action Movie In Strack",
                    img: "src/assets/img/4-1.jpg",
                    date: "February 12,2016",
                    views: "277 Views",
                    number: "2.30.00"
                },
                {
                    title: "Movie Auctor Quisque In Strack",
                    img: "src/assets/img/6.jpg",
                    date: "February 12,2016",
                    views: "300 Views",
                    number: "2.30.00"
                },
                {
                    title: "Auctor Movie Quisque In Strack",
                    img: "src/assets/img/5-1.jpg",
                    date: "February 12,2016",
                    views: "343 Views",
                    number: "2.30.00"
                },
                {
                    title: "Donec Movie Quisque In Strack",
                    img: "src/assets/img/1-2.jpg",
                    date: "February 12,2016",
                    views: "361 Views",
                    number: "2.30.00"
                },
                {
                    title: "New Movie Quisque In Strack",
                    img: "src/assets/img/2-1.jpg",
                    date: "February 12,2016",
                    views: "503 Views",
                    number: "2.30.00"
                }
            ]
        }
    },
    methods: {
        resetDisplay() {
            this.displayScreenDefault = 'd-block';
            this.displayScreenNew = 'd-none';
        },
        toggleScreen() {
            this.resetDisplay();
            setTimeout(() => {
                this.displayScreenDefault = this.displayScreenDefault === 'd-block' ? 'd-none' : 'd-block';
                this.displayScreenNew = this.displayScreenNew === 'd-block' ? 'd-none' : 'd-block';
            }, 1000);
        },
    },
};
</script>
<template>
    <section id="movie-playlist">
        <div class="container py-5">
            <div class="pb-2 ps-3 text-white section-title">
                <h2>{{ section[0].title }}</h2>
                <span>{{ section[0].subtitle }}</span>
            </div>
            <div class="row g-0 pt-4 justify-content-between text-white">
                <div class="col-screen col-screen-default" :class="displayScreenDefault">
                    <div class="background-default">
                        <div class="background-default-top d-flex align-items-center p-3">
                            <div>
                                <img src="../../assets/img/channels4_profile.jpg" alt="logo-channel"
                                    class="logo-channel">
                                <span class="ps-3">Yeh Saali Aashiqui | Official trailer | Verdhan Puri,
                                    Shivaleek...</span>
                            </div>
                            <div class="d-flex">
                                <div class="text-center ps-5">
                                    <i class="fa-solid fa-clock"></i>
                                    <div>Guarda più...</div>
                                </div>
                                <div class="text-center ps-3">
                                    <i class="fa-solid fa-share"></i>
                                    <div>Condividi</div>
                                </div>
                            </div>
                        </div>
                        <div class="background-default-bottom py-2">
                            <span class="text-white">Guarda su</span>
                            <img src="../../assets/img/logo-youtube.webp" class="img-fluid youtube-logo"
                                alt="youtube-logo">
                        </div>
                    </div>
                </div>
                <div class="col-screen col-screen-new" :class="displayScreenNew">
                    <div class="background-new">
                        <div class="background-new-top d-flex align-items-center justify-content-between p-3">
                            <div>
                                <img src="../../assets/img/channels4_profile.jpg" alt="logo-channel"
                                    class="logo-channel">
                                <span class="ps-3">Yeh Saali Aashiqui | Official trailer | Verdhan Puri,
                                    Shivaleek...</span>
                            </div>
                            <div class="d-flex">
                                <div class="text-center ps-5">
                                    <i class="fa-solid fa-clock"></i>
                                    <div>Guarda più...</div>
                                </div>
                                <div class="text-center ps-3">
                                    <i class="fa-solid fa-share"></i>
                                    <div>Condividi</div>
                                </div>
                            </div>
                        </div>
                        <div class="background-new-center h-50 d-flex justify-content-center">
                            <img src="../../assets/img/image (11).svg" alt="img-youtube-video">
                        </div>
                        <div class="background-new-bottom py-2">
                            <span class="text-white">Guarda su</span>
                            <img src="../../assets/img/logo-youtube.webp" class="img-fluid youtube-logo"
                                alt="youtube-logo">
                        </div>
                    </div>
                </div>


                <div class="col-playlist">
                    <div class="playlist-title p-3">
                        <h3>New Movie</h3>
                        <span>Plying 24</span>
                    </div>
                    <div class="playlist-content p-3">
                        <div class="single-playlist d-flex" v-for="movie in movies" :key="movie.title">
                            <div class="playlist-figure pe-3">
                                <img :src="movie.img" :alt="movie.title" class="figure-img">
                            </div>
                            <div class="playlist-content w-100">
                                <h5 @click="toggleScreen" class="m-0 pb-1">{{ movie.title }}</h5>
                                <span class="font-size-small">{{ movie.views }}</span>
                                <div class="font-size-small d-flex justify-content-between">
                                    <div>{{ movie.date }}</div>
                                    <div>{{ movie.number }}</div>
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

#movie-playlist {
    min-height: 500px;
    background-color: $dark-blue;

    .section-title {
        border-bottom: 1px solid $light-blue;
        border-left: 2px solid $primary;
    }

    .col-screen {
        height: 500px;
        width: 66%;
        position: relative;
        display: none;
    }

    // Screen default black
    .col-screen-default {
        background-color: $black;

        .logo-channel {
            border-radius: 50%;
        }

        .background-default-bottom {
            background-color: $dark-grey;
            display: inline-block;
            padding: 5px 10px;
            position: absolute;
            bottom: 5px;
        }

        .youtube-logo {
            filter: invert(1);
            width: 90px;
        }
    }

    // Screen New with movie
    .col-screen-new {
        background-image: url('../../assets/img/maxresdefault.webp');
        background-position: center;
        background-repeat: no-repeat;

        .background-new {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.5);

            .background-new-center img {
                width: 70px;
                cursor: pointer;
            }
        }

        .logo-channel {
            border-radius: 50%;
        }

        .background-new-bottom {
            background-color: $dark-grey;
            display: inline-block;
            padding: 5px 10px;
            position: absolute;
            bottom: 5px;
        }

        .youtube-logo {
            filter: invert(1);
            width: 90px;
        }
    }

    .col-playlist {
        height: 500px;
        width: 31%;
        background-color: $light-blue;

        .playlist-title {
            height: 92px;
            position: sticky;
            border-bottom: 1px solid $dark-blue;
        }

        .playlist-content {
            height: calc(100% - 92px);
            overflow-y: auto;

            h5 {
                cursor: pointer;

                &:hover {
                    color: $primary;
                }
            }

            .figure-img {
                height: 95px;
                width: 95px;
                object-fit: cover;
            }

            .font-size-small {
                font-size: 14px;
            }
        }
    }
}
</style>