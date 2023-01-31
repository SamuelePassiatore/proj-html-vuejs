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
                <div class="d-flex w-50 justify-content-start align-items-center">
                    <i class="fa-regular fa-envelope text-white pe-1"></i>
                    <span class="text-white">Superhit Hot Movie</span>
                    <span class="span-colored pe-3">**King Star**</span>
                    <i class="fa-brands fa-facebook-f text-blue"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-linkedin-in"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-google-plus-g"></i>
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
    </header>
</template>
<style lang="scss" scoped>
header {
    height: 200px;
    background-color: #060F19;

    .header-top {
        height: 40px;
        font-size: 13px;
        border-bottom: 1px solid #182028;

        .span-colored {
            color: #13BE13;
        }

        .fa-brands {
            padding-right: 10px;
        }

        .fa-facebook-f {
            color: #37538F;
        }

        .fa-twitter {
            color: #00ACEE;
        }

        .fa-linkedin-in {
            color: #0D72A2;
        }

        .fa-instagram {
            color: #7D1A23;
        }

        .fa-google-plus-g {
            color: #DB4A39;
        }
    }

    .header-center {
        height: 100px;
        border-bottom: 1px solid #182028;
    }
}
</style>