<script>
export default {
    name: "AppMain"
}
</script>

<template>
    <main>
        <div class="container">
            <h1> &RightArrow; Content goes here &leftarrow; </h1>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

main {
    width: 100%;
    height: 120px;
    background-color: $bg-main-color;

    .container {
        @include flex-center("vertical");

        h1 {
            font-size: 25px;
            color: white;
        }
    }
}
</style>