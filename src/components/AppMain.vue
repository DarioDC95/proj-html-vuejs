<script>
    import AppBusinessSection from './subSectionMain/AppBusinessSection.vue';
    import AppWhatwedoSection from './subSectionMain/AppWhatwedoSection.vue';
    import AppStartyourproject from './subSectionMain/AppStartyourproject.vue';
    import AppSlider from './subSectionMain/AppSlider.vue';
    import AppPricing from './subSectionMain/AppPricing.vue';
    import AppLatestPosts from './subSectionMain/AppLatestPosts.vue';
    import AppTestimonial from './subSectionMain/AppTestimonial.vue';

    export default {
        components: {
            AppBusinessSection,
            AppWhatwedoSection,
            AppStartyourproject,
            AppSlider,
            AppPricing,
            AppLatestPosts,
            AppTestimonial,
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

        <!-- slider -->
        <AppSlider />

        <!-- pricing -->
        <AppPricing />

        <!-- latest post -->
        <AppLatestPosts />

        <!-- testimonial -->
        <AppTestimonial />
    </main>
</template>

<style scoped lang="scss">
    main {
        padding-bottom: 50px;
    }    
</style>