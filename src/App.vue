<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppMain from './components/AppMain.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue'

export default {
    components: {
        AppHeader,
        AppJumbo,
        AppMain,
        AppBanner,
        AppFooter
    }
}
</script>

<template>
    <AppHeader />

    <main>
        <AppJumbo />
        <AppMain />
        <AppBanner />
    </main>

    <AppFooter />
</template>


<style lang="scss">
@use "./styles/general.scss" as *;
</style>