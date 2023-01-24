<script>
    import AppBusinessSection from './AppBusinessSection.vue';
    import AppWhatwedoSection from './AppWhatwedoSection.vue';
    import AppStartyourproject from './AppStartyourproject.vue';

    export default {
        components: {
            AppBusinessSection,
            AppWhatwedoSection,
            AppStartyourproject,
        }
    }
</script>

<template>
    <main>
        <!-- business-planning -->
        <AppBusinessSection />

        <!-- what-we-do -->
        <AppWhatwedoSection />

        <!-- start-your-project -->
        <AppStartyourproject />
    </main>
</template>

<style scoped lang="scss">
    main {
        padding-bottom: 200px;
    }    
</style>