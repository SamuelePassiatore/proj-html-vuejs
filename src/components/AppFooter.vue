<script>
import FooterTop from './footers/FooterTop.vue';
import FooterBottom from './footers/FooterBottom.vue';
export default {
    name: 'AppFooter',
    components: { FooterTop, FooterBottom },
    data() {
        return {

        }
    }
};
</script>

<template>
    <footer-top></footer-top>
    <footer-bottom></footer-bottom>
</template>

<style lang="scss" scoped>

</style>