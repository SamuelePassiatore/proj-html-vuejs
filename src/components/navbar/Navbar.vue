<script>
export default {
    name: 'Navbar',
    data() {
        return {
            navbarItems: ['Home', 'Celebrity', 'Movie', 'Page', 'Shop', 'Blog', 'Contact Us']
        }
    }
};
</script>
<template>
    <nav class="d-flex justify-content-between align-items-center">
        <ul class="d-flex p-0 m-0">
            <li class="align-items-center pe-3" v-for="item in navbarItems" :key="item">
                {{ item }}&blacktriangledown;
            </li>
        </ul>
        <div class="d-flex">
            <i class="fa-solid fa-bag-shopping text-white"></i>
            <div class="circle">
                <span class="circle-number">0</span>
            </div>
        </div>
    </nav>
</template>
<style lang="scss" scoped>
nav {
    height: 60px;

    li {
        list-style-type: none;
        cursor: pointer;
        color: white;

        &:hover {
            color: #2CA6A4;
        }
    }

    .circle {
        width: 17px;
        height: 17px;
        border-radius: 50%;
        background-color: #2CA6A4;
        color: black;
        position: relative;
        bottom: 12px;
        right: 2px;
        text-align: center;
        line-height: 17px;
    }

    .circle-number {
        font-size: 13px;
        color: white;
    }
}
</style>