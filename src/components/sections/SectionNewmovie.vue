<script>
export default {
    name: 'SectionNewmovie',
    data() {
        return {
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
                    category: "Top rating",
                    details: "Details",
                    views: "947 Views",
                    star: "4/10"
                },
                {
                    title: "New Movie Quisque In Strack",
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
                }
            ]
        }
    }
};
</script>
<template>
    <section id="new-movie">
        <div>
            <h2>{{ section[0].title }}</h2>
            <p>{{ section[0].subtitle }}</p>
            <div v-for="movie in movies" :key="movie.title" class="img-fluid">
                <img :src="movie.img">
                <h3>{{ movie.title }}</h3>
                <span>{{ movie.category }}</span>
                <span>{{ movie.details }}</span>
                <span>{{ movie.views }}</span>
                <span>{{ movie.star }}</span>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
#new-movie {
    min-height: 500px;
    background-color: red;
    margin-top: 520px;
}

img {
    width: 100px;
}
</style>