<script>
export default {
    name: "AppHeader",
    data () {
        return {
            linksNav: [
                {
                    title: "CHARACTERS",
                    href: "",
                    active: false,
                },
                {
                    title: "COMICS",
                    href: "",
                    active: true,
                },
                {
                    title: "MOVIE",
                    href: "",
                    active: false,
                },
                {
                    title: "TV",
                    href: "",
                    active: false,
                },
                {
                    title: "GAMES",
                    href: "",
                    active: false,
                },
                {
                    title: "COLLECTIBLES",
                    href: "",
                    active: false,
                },
                {
                    title: "VIDEOS",
                    href: "",
                    active: false,
                },
                {
                    title: "FANS",
                    href: "",
                    active: false,
                },
                {
                    title: "NEWS",
                    href: "",
                    active: false,
                },
                {
                    title: "SHOP",
                    href: "",
                    active: false,
                }

            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo-header">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
            <nav class="nav-header">
                <ul>
                    <li v-for="(link, index) in linksNav" :key="index">
                        <a :class="{'active' : link.active}" href="">{{link.title}}</a>
                    </li>
                    
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

header {
    width: 100%;
    height: $header-height;
    background-color: white;

    .container {
        @include flex-center("vertical");
        position: relative;
        
        .logo-header {
            img {
                width: 80px;
                height: 80px;
            }
        }

        .nav-header {
            
            position: absolute;
            right: 0;

            ul {
                height: 120px;
                list-style-type: none;
                @include flex-center("vertical");

                li {
                    margin: 0 15px;
                    
                    a {
                        color: $secondary-color;
                        font-size: 13px;
                        font-weight: 900;
                        &.active {
                            color: $primary-color;
                            border-bottom: 2px solid $primary-color;
                        }

                    }
                }
            }
        }
    

    }
}
</style>