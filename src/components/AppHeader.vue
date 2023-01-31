<script>
import Navbar from './navbar/Navbar.vue';
import SearchForm from './forms/SearchForm.vue';
export default {
    name: 'AppHeader',
    components: { Navbar, SearchForm },
    data() {
        return {

        }
    }
};
</script>
<template>
    <header>
        <div class="container">
            <div class="header-top d-flex">
                <div class="d-flex w-50 bg-warning justify-content-start align-items-center">
                    <i class="fa-regular fa-envelope"></i>
                    <span>Superhit Hot Movie ** King Star **</span>
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-linkedin-in"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-google-plus-g"></i>
                </div>
                <div class="d-flex w-50 bg-danger justify-content-end align-items-center">
                    <i class="fa-solid fa-lock"></i>
                    <span>Login</span>
                </div>
            </div>
            <div class="header-center d-flex align-items-center">
                <figure class="m-0">
                    <img src="../assets/img/cropped-logo.png" alt="logo">
                </figure>
                <search-form></search-form>
            </div>
            <div class="header-menu">
                <navbar></navbar>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
header {
    height: 200px;
    background-color: #060F19;

    .header-top {
        height: 40px;
    }

    .header-center {
        height: 100px;
    }
}
</style>