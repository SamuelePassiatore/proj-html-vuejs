<script>
import { store } from './assets/data/store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
    components: { AppHeader, AppMain, AppFooter },
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
    <app-footer></app-footer>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>