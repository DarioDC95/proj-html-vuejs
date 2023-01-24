<script>
    import AppBusinessSection from './AppBusinessSection.vue';
    import AppWhatwedoSection from './AppWhatwedoSection.vue';

    export default {
        components: {
            AppBusinessSection,
            AppWhatwedoSection,
        }
    }
</script>

<template>
    <main>
        <!-- business-planning -->
        <AppBusinessSection />

        <!-- what-we-do -->
        <AppWhatwedoSection />
    </main>
</template>

<style scoped lang="scss">
    main {
        padding-bottom: 200px;
    }    
</style>