<script>
export default {
    name: 'MoviesCard',
    props: {
        movie: Object
    }
};
</script>
<template>
    <div>
        <img :src="movie.img">
        <h3>{{ movie.title }}</h3>
        <span>{{ movie.category }}</span>
        <span>{{ movie.details }}</span>
        <span>{{ movie.views }}</span>
        <span>{{ movie.star }}</span>
    </div>
</template>
<style lang="scss" scoped>

</style>