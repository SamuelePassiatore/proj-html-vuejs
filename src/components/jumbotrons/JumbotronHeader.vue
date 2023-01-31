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
        <div class="jumbotron-header-content text-white">
            <span>Welcome</span>
            <h2>OUR SPECIAL <span class="title-colored">MOVIES</span></h2>
            <p class="paragraph-jumbotron text-center">Lorem Ipsum is Simply dummy text of the printing and typesetting
                industrioy.
                Lorem
                Ipsum has
                been the
                industry standard dummy text ever since the 1500s, when an unknown</p>
            <button class="text-white border-0 rounded-5 px-4 py-2">Read More</button>
        </div>
        <i class="fa-solid fa-arrow-right fa-2x pe-5"></i>
    </div>
</template>
<style lang="scss" scoped>
.jumbotron-header {
    height: 520px;
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

    .jumbotron-header-content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100%;
        padding-left: 300px;
    }

    .title-colored {
        color: #13BE13;
    }

    .paragraph-jumbotron {
        width: 40%;
    }



    button {
        background-color: #13BE13;
    }
}
</style>