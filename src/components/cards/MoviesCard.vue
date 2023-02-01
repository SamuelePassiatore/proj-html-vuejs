<script>
export default {
    name: 'MoviesCard',
    props: {
        movie: Object
    }
};
</script>
<template>
    <div class="col-2">
        <div class="card-custom">
            <img :src="movie.img" class="card-image rounded-5 w-100">
            <div class="card-body">
                <h3>{{ movie.title }}</h3>
                <span>{{ movie.category }}</span>
                <span>{{ movie.details }}</span>
                <span>{{ movie.views }}</span>
                <span>{{ movie.star }}</span>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.card-custom {
    position: relative;
}

.card-image {
    height: 500px;
}

.card-body {
    position: absolute;
    bottom: 30px;
}
</style>