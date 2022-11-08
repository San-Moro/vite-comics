<script>
export default {
    name: "AppFooter"
}
</script>

<template>
    <footer>
        <div class="container">
            <h1>Footer</h1>
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

        h1 {
            font-size: 25px;
            color: white;
        }
    }
}
</style>