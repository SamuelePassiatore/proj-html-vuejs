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
    <nav>
        <ul>
            <li v-for="item in navbarItems" :key="item">{{ item }}</li>
        </ul>
    </nav>
</template>
<style lang="scss" scoped>

</style>