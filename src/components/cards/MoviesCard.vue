<script>
export default {
    name: 'MoviesCard',
    props: {
        movie: Object
    }
};
</script>
<template>
    <div class="card-custom">
        <img :src="movie.img" class="card-image">
        <div class="card-body">
            <h3>{{ movie.title }}</h3>
            <span>{{ movie.category }}</span>
            <span>{{ movie.details }}</span>
            <span>{{ movie.views }}</span>
            <span>{{ movie.star }}</span>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.card-custom {
    display: flex;
    width: calc(100% / 3);
    height: 500px;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
    position: relative;
}

.card-image {
    width: 100%;
    object-fit: cover;
}

.card-body {
    position: absolute;
    bottom: 20px;
}
</style>