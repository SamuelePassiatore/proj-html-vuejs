<script>
import JumbotronMain from './jumbotrons/JumbotronMain.vue';
import SectionNewmovie2 from './sections/SectionNewmovie2.vue';
export default {
    name: 'AppMain',
    components: { JumbotronMain, SectionNewmovie2 },
    data() {
        return {

        }
    }
};
</script>
<template>
    <section-newmovie2></section-newmovie2>
    <jumbotron-main></jumbotron-main>
</template>
<style lang="scss" scoped>

</style>