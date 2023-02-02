<script>
export default {
    name: 'FooterBottom',
    data() {
        return {
            footerElements: ['Tram and Conditions', 'Policy', 'About'],
        }
    }
}
</script>

<template>
    <div class="footer-bottom d-flex align-items-center">
        <!-- Container with flex -->
        <div class="container d-flex justify-content-between">
            <!-- Footer bottom left -->
            <div class="elements">
                <ul class="d-flex">
                    <li class="pe-5" v-for="footerElement in footerElements" :key="footerElement">{{ footerElement }}
                    </li>
                </ul>
            </div>
            <!-- Footer bottom right -->
            <div class="copyright">
                <span><i class="fa-regular fa-copyright"></i></span>
                <span>2020</span>
                <span class="text-colored px-1">@Themepul</span>
                <span>All Rights Reserved.</span>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.footer-bottom {
    background-color: $dark-blue;
    min-height: 60px;
    color: white;

    .text-colored {
        color: $primary;
    }
}
</style>