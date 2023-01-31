<script>
export default {
    name: 'JumbotronHeader',
    data() {
        return {

        }
    }
};
</script>
<template>
    <div class="jumbotron-header">
        <i class="fa-solid fa-arrow-left fa-2x ps-5"></i>
        <i class="fa-solid fa-arrow-right fa-2x pe-5"></i>
    </div>
</template>
<style lang="scss" scoped>
.jumbotron-header {
    height: 450px;
    background-image: url('../../assets/img/slider-1024x347.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;

    .fa-solid {
        position: absolute;
        top: 50%;
        transform: translate(0, -50%);
        color: #fff;
        cursor: pointer;

        &:hover {
            color: #13BE13;
        }
    }

    .fa-arrow-right {
        right: 0;
    }
}
</style>