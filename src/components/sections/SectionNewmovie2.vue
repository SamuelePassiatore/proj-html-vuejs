<script>
export default {
    name: 'SectionNewmovie2',
    data() {
        return {
            NewMovie2: [
                { title: "Hurry Animate Blue Strack New Movie", img: "", category: "Top rating", details: "Details", views: "381 Views", star: "0/10" },
                { title: "Animate Blue Strack New Movie", img: "", category: "Latest Movie", details: "Details", views: "343 Views", star: "0/10" },
                { title: "Blue Strack New Animate Movie", img: "", category: "Coming Soon", details: "Details", views: "420 Views", star: "0/10" },
                { title: "Nulla Strack New Animate Movie", img: "", category: "Tv Series", details: "Details", views: "324 Views", star: "0/10" },
                { title: "Quisque In Strack New Movie", img: "", category: "Top rating", details: "Details", views: "339 Views", star: "1/10" },
                { title: "New Movie Quisque In Strack", img: "", category: "Latest Movie", details: "Details", views: "503 Views", star: "1/10" },
            ]
        }
    }
};
</script>
<template>
    <section id="new-movie-2">
        <div>
            <div class="d-flex" v-for="movie in NewMovie2" :key="movie.title">
                <h3>{{ movie.title }}</h3>
                <p>Category: {{ movie.category }}</p>
                <p>Details: {{ movie.details }}</p>
                <p>Views: {{ movie.views }}</p>
                <p>Star: {{ movie.star }}</p>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
#new-movie-2 {
    height: 400px;
}
</style>