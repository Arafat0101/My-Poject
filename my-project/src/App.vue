<template>
  <div id="app">

    <!-- PREMIUM FEATURES BUTTON -->
    <a target="_blank" class="hide-s" href="../template/prospera-premium-responsive-business-template/" style="position:fixed;top:120px;right:-14px;z-index:10;"><img src="dist/img/premium-features.png" alt=""></a>
    <!-- HEADER -->
    <header role="banner">
      <!-- Top Bar -->
      <div class="top-bar background-white">
        <div class="line">
          <div class="s-12 m-6 l-6">
            <div class="top-bar-contact">
              <p class="text-size-12">Contact Us: 01717 38 28 92 | <a class="text-orange-hover" href="mailto:arafat2892@gmail.com">arafat2892@gmail.com</a></p>
            </div>
          </div>
          <div class="s-12 m-6 l-6">
            <div class="right">
              <ul class="top-bar-social right">
                <li><a href="/"><i class="icon-facebook_circle text-orange-hover"></i></a></li>
                <li><a href="/"><i class="icon-twitter_circle text-orange-hover"></i></a> </li>
                <li><a href="/"><i class="icon-google_plus_circle text-orange-hover"></i></a></li>
                <li><a href="/"><i class="icon-instagram_circle text-orange-hover"></i></a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Top Navigation -->
      <nav class="background-white background-primary-hightlight">
        <div class="line">
          <div class="s-12 l-2">
            <a href="/" class="logo"><img src="dist/img/logo-free.png" alt=""></a>
          </div>
          <div class="top-nav s-12 l-10">
            <p class="nav-text"></p>
            <ul class="right chevron">
              <li><router-link to="/">Home</router-link> </li>
              <li><router-link to="/about">About</router-link> </li>
              <li><router-link to="/product">Product</router-link> </li>
              <li><router-link to="/gallery">Gallery</router-link> </li>
              <li><router-link to="/contact">Contact</router-link> </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>

    <!-- MAIN -->
    <router-view></router-view>


  </div>
</template>

<script>
import VueRouter from 'vue-router'
import Home from './pages/Home'
import About from './pages/About'
import Product from './pages/Product'
import Gallery from './pages/Gallery'
import Contact from './pages/Contact'

const routes = [
    { path: '/', component: Home },
    { path: '/about', component: About },
    { path: '/product', component: Product },
    { path: '/gallery', component: Gallery },
    { path: '/contact', component: Contact }
  ]


  const router = new VueRouter({
    routes,
    mode: 'history'
  })




export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  router
}
</script>
