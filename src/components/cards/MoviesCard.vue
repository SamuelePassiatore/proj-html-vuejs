<script>
export default {
    name: 'MoviesCard',
    props: {
        movie: Object
    }
};
</script>
<template>
    <div class="col-4 position-relative">
        <div class="card-custom">
            <img :src="movie.img" class="card-image rounded-5 w-100">
            <div class="card-body text-white">
                <h3 class="card-title">{{ movie.title }}</h3>
                <span class="card-category">{{ movie.category }}</span>
                <span class="card-details">{{ movie.details }}</span>
                <span class="card-views">{{ movie.views }}</span>
                <span class="card-star"><i class="fa-solid fa-star text-colored pe-1"></i>{{ movie.star }}</span>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.card-image {
    height: 500px;
    filter: brightness(0.6);
    border: 3px solid transparent;
}

.text-colored {
    color: #2CA6A4;
}

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
    background-color: #060F19;
    border-top-left-radius: 18px;
    border-bottom-left-radius: 18px;
}

.card-details {
    position: absolute;
    bottom: 25px;
    left: 0;
    padding: 4px 12px;
    background-color: #060F19;
    border-top-right-radius: 18px;
    border-bottom-right-radius: 18px;
}

.card-star {
    position: absolute;
    top: 20px;
    right: 10px;
}
</style>