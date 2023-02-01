<script>
export default {
    name: 'SectionMovieplaylist',
    data() {
        return {
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
    }
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
                <div class="col-screen">
                    <div class="background-default">
                        <div class="background-default-top d-flex align-items-center p-3">
                            <div>
                                <img src="../../assets/img/channels4_profile.jpg" alt="logo-channel"
                                    class="logo-channel">
                                <span class="ps-3">Yeh Saali Aashiqui | Official trailer | Verdhan Puri,
                                    Shivaleek...</span>
                            </div>
                            <div class="text-center ps-5">
                                <i class="fa-solid fa-clock"></i>
                                <div>Guarda più...</div>
                            </div>
                            <div class="text-center ps-3">
                                <i class="fa-solid fa-share"></i>
                                <div>Condividi</div>
                            </div>
                        </div>
                        <div class="background-default-bottom">
                            <span class="text-white">Guarda su</span>
                            <img src="../../assets/img/logo-youtube.webp" class="img-fluid youtube-logo"
                                alt="youtube-logo">
                        </div>
                    </div>
                    <div class="video-background">

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
                                <h5 class="m-0 pb-1">{{ movie.title }}</h5>
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
#movie-playlist {
    min-height: 500px;
    background-color: #060F19;

    .section-title {
        border-bottom: 1px solid #182028;
        border-left: 2px solid #13BE13;
    }

    .col-screen {
        height: 500px;
        width: 66%;
        background-color: black;
        position: relative;

        .logo-channel {
            border-radius: 50%;
        }

        .background-default-bottom {
            background-color: #121212;
            display: inline-block;
            padding: 5px 10px;
            position: absolute;
            bottom: 3px;
        }

        .youtube-logo {
            filter: invert(1);
            width: 90px;
        }
    }

    .col-playlist {
        height: 500px;
        width: 31%;
        background-color: #182028;

        .playlist-title {
            height: 92px;
            position: sticky;
            border-bottom: 1px solid #060F19;
        }

        .playlist-content {
            height: calc(100% - 92px);
            overflow-y: auto;

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