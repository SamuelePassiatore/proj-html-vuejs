<script>
export default {
    name: 'FooterTop',
    data() {
        return {
            about: [
                {
                    title: 'About Us',
                    paragraph: 'Mauris malesuada arcu eu posuere eleifen. Ut egestas tortor at leo egestas tincidunt. Nam tincidunt metus tristique tristique viverra. Mauris erat ante, egestas vitae dapibus seds.'
                }
            ],
            categoryList: ['English New Movie', 'Hindi All Movie', 'Latest Tamil Movie', 'New Top Rating Movie', 'Hornn New Movie', 'Animation New Movie'],
            informations: ['Youtube Video Post', 'Actor Information', 'New Promotion', 'Latest Movie In English', 'Latest Flim Product', 'Video New Video'],
            recentPosts: [
                {
                    img: 'src/assets/img/blog-100x100.jpg',
                    title: 'Actor The Concept Movie High Concept Theory see',
                    date: 'April 14, 2020'
                },
                {
                    img: 'src/assets/img/blog2-100x100.jpg',
                    title: 'consequat Nam lectus nibh aucibus It has turpis',
                    date: 'April 14, 2020'
                },
                {
                    img: 'src/assets/img/blog3-100x100.jpg',
                    title: 'Nam lectus nibh consequat aucibus turpis',
                    date: 'April 14, 2020'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="footer-top">
        <!-- Dark overlay -->
        <div class="overlay">
            <!-- Container flex -->
            <div class="container d-flex">
                <!-- About us -->
                <div class="about text-white w-25 py-5 pe-5">
                    <h3 class="m-0">{{ about[0].title }}</h3>
                    <!-- White line -->
                    <div class="border-bottom mb-4"></div>
                    <p class="pb-2">{{ about[0].paragraph }}</p>
                    <div class="icons d-flex">
                        <a href="#" class="facebook-circle"><i class="fa-brands fa-facebook-f text-blue"></i></a>
                        <a href="#" class="twitter-circle"><i class="fa-brands fa-twitter"></i></a>
                        <a href="#" class="linkedin-circle"><i class="fa-brands fa-linkedin-in"></i></a>
                        <a href="#" class="instagram-circle"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#" class="pinterest-circle"><i class="fa-brands fa-pinterest"></i></a>
                    </div>
                </div>
                <!-- Movie category -->
                <div class="movie-category text-white w-25 py-5 px-5">
                    <h3 class="m-0">Movie Category</h3>
                    <div class="border-bottom mb-4"></div>
                    <ul>
                        <!-- List with for cycle -->
                        <li class="pb-4" v-for="category in categoryList" :key="category">{{ category }}</li>
                    </ul>
                </div>
                <!-- Information -->
                <div class="information text-white w-25 py-5 px-5">
                    <h3 class="m-0">Information</h3>
                    <div class="border-bottom mb-4"></div>
                    <ul>
                        <li class="pb-4" v-for="information in informations" :key="information">{{ information }}</li>
                    </ul>
                </div>
                <!-- Recent post -->
                <div class="recent-post text-white w-25 py-5 ps-5">
                    <h3 class="m-0">Recent Post</h3>
                    <div class="border-bottom mb-4"></div>
                    <div v-for="recentPost in recentPosts" :key="recentPost.title" class="d-flex pb-4">
                        <img :src="recentPost.img" :alt="recentPost.title">
                        <div class="pt-2 ps-3 content-recent-post">
                            <h5 class="font-smaller lh-lg">{{ recentPost.title }}</h5>
                            <span class="font-smaller">{{ recentPost.date }}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.footer-top {
    position: relative;
    background-image: url('../../assets/img/ft-bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    min-height: 500px;

    .overlay {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(24, 32, 40, 0.93);
    }

    // White line
    .border-bottom {
        background-color: $white;
        height: 2px;
        width: 35px;
    }

    // About us 
    a {
        text-decoration: none;
        width: 40px;
        height: 40px;
        border-radius: 50%;
        margin-right: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .fa-brands {
        color: $white;
    }

    // Icons with div circle
    .facebook-circle {
        background-color: $blue-facebook;
    }

    .twitter-circle {
        background-color: $blue-twitter;
    }

    .linkedin-circle {
        background-color: $blue-linkedin;
    }

    .instagram-circle {
        background-color: $orange;
    }

    .pinterest-circle {
        background-color: $red;
    }

    // Recent posts 

    .font-smaller {
        font-size: 14px;
    }



}
</style>