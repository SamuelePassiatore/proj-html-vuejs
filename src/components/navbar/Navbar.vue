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
            <li class="text-white align-items-center" v-for="item in navbarItems" :key="item">
                {{ item }}&blacktriangledown;
            </li>
        </ul>
        <div><i class="fa-solid fa-bag-shopping"></i></div>
    </nav>
</template>
<style lang="scss" scoped>
nav {
    height: 60px;
    background-color: green;

    li {
        list-style-type: none;
    }
}
</style>