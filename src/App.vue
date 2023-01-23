<script>
  import AppHeader from './components/AppHeader.vue'
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';
  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter
    },
    data() {
      return {
        link_menu: [
          {
            label: 'Home',
            url: '#',
            active: true
          },
          {
            label: 'About',
            url: '#',
            active: false
          },
          {
            label: 'Services',
            url: '#',
            active: false
          },
          {
            label: 'Blog',
            url: '#',
            active: false
          },
          {
            label: 'Contact',
            url: '#',
            active: false
          },
          {
            label: 'Portfolio',
            url: '#',
            active: false
          },
        ],
      }
    }
  }
</script>

<template>
  <AppHeader :menu="link_menu" />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/general' as *;

</style>
