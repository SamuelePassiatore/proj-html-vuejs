<script>
import { store } from './assets/data/store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import JumbotronHeader from './components/jumbotrons/JumbotronHeader.vue';
import JumbotronMain from './components/jumbotrons/JumbotronMain.vue';
import SearchForm from './components/forms/SearchForm.vue';
import SendForm from './components/forms/SendForm.vue';
import Navbar from './components/navbar/Navbar.vue';
import SectionNewmovie from './components/sections/SectionNewmovie.vue';
import SectionNewmovie2 from './components/sections/SectionNewmovie2.vue';
import SectionMovieplaylist from './components/sections/SectionMovieplaylist.vue';
import SectionLatestnews from './components/sections/SectionLatestnews.vue';
export default {
    components: {
        AppHeader, AppMain, AppFooter, JumbotronHeader, JumbotronMain, SearchForm, SendForm,
        Navbar, SectionNewmovie, SectionNewmovie2, SectionMovieplaylist, SectionLatestnews
    },
    data() {
        return {
            store,
        }
    }
};
</script>
<template>
    <app-header></app-header>
    <app-main></app-main>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>