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
        link_footer: [
          {
            title: 'Quick Links',
            links: [
              {
                label: 'Services',
                url: '#'
              },
              {
                label: 'Contact',
                url: '#'
              },
              {
                label: 'Blog',
                url: '#'
              },
            ]
          },
          {
            title: 'Resources',
            links: [
              {
                label: 'Art Design',
                url: '#'
              },
              {
                label: 'Computer',
                url: '#'
              },
              {
                label: 'IT News',
                url: '#'
              },
              {
                label: 'Networking',
                url: '#'
              },
              {
                label: 'Web Security',
                url: 'null#'
              },
            ]
          }
        ]
      }
    },
    methods: {
      changeMenu(value) {
        for(let i = 0; i < this.link_menu.length; i++) {
          this.link_menu[i].active = false;
        }
        this.link_menu[value].active = true;
      }
    }
  }
</script>

<template>
  <AppHeader @selection="changeMenu" :menu="link_menu" />
  <AppMain />
  <AppFooter :footerLink="link_footer"/>
</template>

<style lang="scss">
@use './styles/general' as *;

</style>
