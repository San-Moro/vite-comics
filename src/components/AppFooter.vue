<script>
export default {
    name: "AppFooter",
    data() {
        return {
            socialIcons: [
                {
                    img: 'footer-facebook.png',
                },
                {
                    img: 'footer-twitter.png',
                },
                {
                    img: 'footer-youtube.png',
                },
                {
                    img: 'footer-pinterest.png',
                },
                {
                    img: 'footer-periscope.png',
                },
                
            ]
        }
    },
    methods: {
        getImageUrl(url) {
            return new URL(url, import.meta.url).href;
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <nav class="nav-footer">

            </nav>
            <div class="footer-bottom">
                <div class="btn btn-footer">
                    <a href="#">sign-up now!</a>
                </div>
                <div class="social-icons" >
                    <h2>Follow us</h2>
                    <a href="" v-for="(icon, index) in socialIcons" :key="index">
                        <img :src="getImageUrl(`../assets/img/${icon.img}`)" alt="">
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

footer {
    width: 100%;
    height: $footer-height;
    background-color: $secondary-color;

    .container {
        @include flex-center("vertical");
        flex-direction: column;

        .nav-footer {
            width: 100%;
            height: 300px;
            border: 1px solid white;
        }

        .footer-bottom {
            width: 100%;
            padding: 30px 0;
            border: 1px solid red;
            @include flex-center("vertical");
            justify-content: space-between;

            .btn-footer {
                border: 2px solid $primary-color;
                font-size: 16px;
                padding: 15px 20px;

                a {
                    color: white;
                }
            }

            .social-icons {
                @include flex-center("both");

                h2 {
                    color: $primary-color;
                    text-transform: uppercase;
                    font-size: 20px;
                    padding-right: 20px;
                }

                img {
                    padding: 0 8px;
                    vertical-align: middle;
                }
            }
                
        }
    }
}
</style>