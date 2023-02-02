<script>
export default {
    name: 'JumbotronMain',
    data() {
        return {

        }
    }
};
</script>
<template>
    <div class="jumbotron-main">
        <div class="jumbotron-main-content text-white">
            <span class="colored">COMING SOON MOVIE</span>
            <h2 class="fs-1">MAX STILL</h2>
            <div class="countdown-text text-center py-1 px-4">
                <div class="fw-bold pb-2">JOHN PLAYER <span class="colored">&</span> EMILY ROSE</div>
                <div>THE COUNTDOWN IS FINISHED!</div>
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.jumbotron-main {
    height: 500px;
    background-image: url('../../assets/img/coming-bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;


    .jumbotron-main-content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
        padding-left: 300px;

        .colored {
            color: $primary;
        }

        .countdown-text {
            background-color: $light-blue;
            font-size: 13px;
        }
    }


}
</style>