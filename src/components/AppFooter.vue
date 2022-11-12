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
            ],
            linksNavFooter: [
                {
                    title: "CHARACTERS",
                    href: "",
                },
                {
                    title: "COMICS",
                    href: "",
                },
                {
                    title: "MOVIE",
                    href: "",
                },
                {
                    title: "TV",
                    href: "",
                },
                {
                    title: "GAMES",
                    href: "",
                },
                {
                    title: "COLLECTIBLES",
                    href: "",
                },
                {
                    title: "VIDEOS",
                    href: "",
                },
                {
                    title: "FANS",
                    href: "",
                },
                {
                    title: "NEWS",
                    href: "",
                },
                {
                    title: "SHOP",
                    href: "",
                }

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
        <nav class="nav-footer">
            <div class="container">
                <div class="menu-footer">
                    <div class="col">
                        <h3>Dc Comics</h3>
                        <ul v-for="(linkNav, index) in linksNavFooter" :key="index"> 
                            <li>
                                <a href="">{{linkNav.title}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <h3>Dc Comics</h3>
                        <ul v-for="(linkNav, index) in linksNavFooter" :key="index"> 
                            <li>
                                <a href="">{{linkNav.title}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <h3>Dc Comics</h3>
                        <ul v-for="(linkNav, index) in linksNavFooter" :key="index"> 
                            <li>
                                <a href="">{{linkNav.title}}</a>
                            </li>
                        </ul>
                    </div>
                
                </div>
                <div class="logo-bg-footer">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </nav>
        <div class="footer-bottom">
            <div class="container">
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
    background-color: $secondary-color;

    
    .nav-footer {
        width: 100%;
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;

        .container {
            display: flex;
            justify-content: space-between ;

            .menu-footer {
                width: 40%;
                padding: 30px 0;
                display: flex;
                .col {
                    padding-right: 40px;

                    h3 {
                        color: white;
                        text-transform: uppercase;
                        font-size: 16px;
                        padding-bottom: 15px;
                    }
                }

                li {
                    text-transform: lowercase;
                    a {
                        color: grey;

                    }
                }
            }

            .logo-bg-footer {
                width: 40%;

                img {
                    transform: scale(1.2);
                }
            }  
        }

    }
    .footer-bottom {
        width: 100%;
        background-color: $secondary-color;
        @include flex-center("vertical");
        flex-direction: column;
        position: absolute;
        z-index: 999;

        .container {
            padding: 30px 0;
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