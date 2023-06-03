<script>
    import AppHeader from './components/AppHeader.vue'
    import MemGenerator from './components/MemGenerator.vue'
    import AppFooter from './components/AppFooter.vue'
    export default {
        components: {
            AppHeader,
            MemGenerator,
            AppFooter,
        }
    }
</script>

<!-- Ссылка для мема: https://www.meme-arsenal.com/memes/048348d157ac1073c62e7a3773555349.jpg -->

<template>
    <app-header />
    <div class="container my-5">
        <mem-generator />
    </div>
    <app-footer />
</template>

<style scoped>

</style>
