<script>
export default {
    name: "AppBanner",
    data() {
        return {
            icons: [
                {
                    image: 'buy-comics-digital-comics.png',
                    title: "Digital comics"
                },
                {
                    image: 'buy-comics-merchandise.png',
                    title: "Dc merchandise"
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    title: "Comic shop locator"
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    title: "Subscription"
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    title: "DC Power Visa"
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
    <section class="banner">
        <div class="container-banner">
            <div class="col">
                <div class="item" v-for="(icon, index) in icons" :key="index">
                    <img :src="getImageUrl(`../assets/img/${icon.image}`)" alt="">
                    <h3>{{ icon.title }}</h3>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.banner {
    width: 100%;
    height: 170px;
    background-color: $primary-color;
    @include flex-center("vertical");

    .container-banner {
        width: 65%;
        margin: 0 auto;
        .col {
            @include flex-center("both");
            .item {
                width: 100%;
                @include flex-center("both");


                img {
                    width: 40px;
                }

                h3 {
                    font-size: 15px;
                    font-weight: 400;
                    color: white;
                    margin-left: 20px;
                    text-transform: uppercase;
                }
            }
        }
    }
}
</style>