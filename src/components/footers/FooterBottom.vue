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
        <div class="container d-flex justify-content-between">
            <div class="elements">
                <ul class="d-flex">
                    <li class="pe-5" v-for="footerElement in footerElements" :key="footerElement">{{ footerElement }}
                    </li>
                </ul>
            </div>
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
.footer-bottom {
    background-color: #060F19;
    min-height: 60px;
    color: white;

    .text-colored {
        color: #2CA6A4;
    }
}
</style>