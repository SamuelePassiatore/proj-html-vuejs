<script>
import SectionNewmovie from './sections/SectionNewmovie.vue';
import SectionMovieplaylist from './sections/SectionMovieplaylist.vue';
import JumbotronMain from './jumbotrons/JumbotronMain.vue';
import SectionNewmovie2 from './sections/SectionNewmovie2.vue';
import SectionLatestnews from './sections/SectionLatestnews.vue';
export default {
    name: 'AppMain',
    components: { SectionNewmovie, SectionMovieplaylist, JumbotronMain, SectionNewmovie2, SectionLatestnews },
    data() {
        return {

        }
    }
};
</script>
<template>
    <section-newmovie></section-newmovie>
    <section-movieplaylist></section-movieplaylist>
    <jumbotron-main></jumbotron-main>
    <section-newmovie2></section-newmovie2>
    <section-latestnews></section-latestnews>
</template>
<style lang="scss" scoped>

</style>