<script>
export default {
    name: "AppBanner"
}
</script>

<template>
    <section class="banner">
        <div class="container-banner">
            <div class="col">
                <div class="item">
                    <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                    <h3>DIGITAL COMICS</h3>
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

    .container-banner {
        width: 65%;
        margin: 0 auto;
        .col {
            .item {
                width: 100%;
                height: $banner-height;
                @include flex-center("vertical");

                img {
                    width: 50px;
                }

                h3 {
                    font-size: 15px;
                    font-weight: 400;
                    color: white;
                    margin-left: 20px;
                }
            }
        }
    }
}
</style>