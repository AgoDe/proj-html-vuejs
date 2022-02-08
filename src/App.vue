<template>
  <div id="app">

      <!-- header container -->
      <header-container
      :navItem="navItem"
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
          path: 'home.png',
          active: false,
          pathActive:'home-2.png',
        },
        {
          item: 'Pages',
          path: 'document.png',
          active: true,
          pathActive:'document-2.png',

        },
        {
          item: 'blog',
          path: 'printer.png',
          active: false,
          pathActive:'printer-2.png',

        },
        {
          item: 'Shop',
          path: 'cart.png',
          active: false,
          pathActive:'cart-2.png',

        },
        {
          item: 'Shortcodes',
          path: 'lab.png',
          active: false,
          pathActive:'lab-2.png',

        },
        {
          item: 'Support',
          path: 'chat.png',
          active: false,
          pathActive:'chat-2.png',

        },
        {
          item: 'Contact',
          path: 'envelope.png',
          active: false,
          pathActive:'envelope-2.png',

        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import '@/styles/main.scss';

</style>
