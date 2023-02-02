<script>
import Navbar from './navbar/Navbar.vue';
import SearchForm from './forms/SearchForm.vue';
import JumbotronHeader from './jumbotrons/JumbotronHeader.vue';
export default {
    name: 'AppHeader',
    components: { Navbar, SearchForm, JumbotronHeader },
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
                <div class="d-flex w-50 justify-content-start align-items-center">
                    <i class="fa-regular fa-envelope text-white pe-1"></i>
                    <span class="text-white">Superhit Hot Movie</span>
                    <span class="span-colored pe-3">**King Star**</span>
                    <a href="#"><i class="fa-brands fa-facebook-f text-blue"></i></a>
                    <a href="#"><i class="fa-brands fa-twitter"></i></a>
                    <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-google-plus-g"></i></a>
                </div>
                <div class="d-flex w-50 justify-content-end align-items-center">
                    <i class="fa-solid fa-lock text-white"></i>
                    <span class="text-white ps-1 pt-1">Login</span>
                </div>
            </div>
            <div class="header-center d-flex align-items-center justify-content-between">
                <figure class="m-0">
                    <img src="../assets/img/cropped-logo.png" alt="logo">
                </figure>
                <search-form></search-form>
            </div>
            <div class="header-menu">
                <navbar></navbar>
            </div>
        </div>
        <jumbotron-header></jumbotron-header>
    </header>
</template>
<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

header {
    height: 200px;
    background-color: $dark-blue;

    a {
        text-decoration: none;
    }

    .header-top {
        height: 40px;
        font-size: 13px;
        border-bottom: 1px solid $light-blue;

        .span-colored {
            color: $primary;
        }

        .fa-brands {
            padding-right: 10px;
        }

        .fa-instagram {
            color: #7D1A23;
        }
    }

    .header-center {
        height: 100px;
        border-bottom: 1px solid $light-blue;
    }
}
</style>