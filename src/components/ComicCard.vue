<script>
export default {
    name: "ComicCard",
    props: {
        image: String,
        title: String
    }

}
</script>

<template>
    <div class="card">
        <img :src="image">
        <h3>{{ title }}</h3>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.card {
    width: calc(100% / 6 - 20px);
    padding: 15px 0;

    h3 {
        font-size: 16px;
        font-weight: 400;
        color: white;
        text-transform: uppercase;
    }
}


</style>