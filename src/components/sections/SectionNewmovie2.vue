<script>
export default {
    name: 'SectionNewmovie2',
    data() {
        return {
            NewMovie2: [
                { Title: "Hurry Animate Blue Strack New Movie", img: "", Category: "Top rating", Details: "Details", Views: "381 Views", Star: "0/10" },
                { Title: "Animate Blue Strack New Movie", img: "", Category: "Latest Movie", Details: "Details", Views: "343 Views", Star: "0/10" },
                { Title: "Blue Strack New Animate Movie", img: "", Category: "Coming Soon", Details: "Details", Views: "420 Views", Star: "0/10" },
                { Title: "Nulla Strack New Animate Movie", img: "", Category: "Tv Series", Details: "Details", Views: "324 Views", Star: "0/10" },
                { Title: "Quisque In Strack New Movie", img: "", Category: "Top rating", Details: "Details", Views: "339 Views", Star: "1/10" },
                { Title: "New Movie Quisque In Strack", img: "", Category: "Latest Movie", Details: "Details", Views: "503 Views", Star: "1/10" },
            ]
        }
    }
};
</script>
<template>
    <section id="new-movie-2">
        <div>
            <div v-for="movie in NewMovie2" :key="movie.Title">
                <h3>{{ movie.Title }}</h3>
                <p>Category: {{ movie.Category }}</p>
                <p>Details: {{ movie.Details }}</p>
                <p>Views: {{ movie.Views }}</p>
                <p>Star: {{ movie.Star }}</p>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>

</style>