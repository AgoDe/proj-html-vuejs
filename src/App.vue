<template>
  <div id="app">

      <!-- header container -->
      <header-container
      />
      <!-- end of header container -->

      <!-- main container  -->
      <main-container
      />
      <!-- end of main container  -->

      <!-- footer container  -->
      <footer-container
      />
      <!-- end of footer container  -->


  </div>
</template>

<script>
import FooterContainer from './components/FooterContainer.vue'
import HeaderContainer from './components/HeaderContainer.vue'
import MainContainer from './components/MainContainer.vue'


export default {
  name: 'App',
  components: {
    HeaderContainer,
    MainContainer,
    FooterContainer
  },
  data() {
    return {
      // Array for navbar items
      navItem: [
        {
          item: 'Home',
          path: 'home-2.png',
          active: true,
          pathActive:'home.png',
        },
        {
          item: 'Pages',
          path: 'document-2.png',
          active: false,
          pathActive:'document.png',

        },
        {
          item: 'blog',
          path: 'printer-2',
          active: true,
          pathActive:'printer.png',

        },
        {
          item: 'Shop',
          path: 'cart-2.png',
          active: true,
          pathActive:'cart.png',

        },
        {
          item: 'Shortcodes',
          path: 'lab-2.png',
          active: true,
          pathActive:'lab.png',

        },
        {
          item: 'Support',
          path: 'chat-2.png',
          active: true,
          pathActive:'chat.png',

        },
        {
          item: 'Contact',
          path: 'envelope-2.png',
          active: true,
          pathActive:'envelope.png',

        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import '@/styles/main.scss';

</style>
