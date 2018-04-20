<template>
  <div id="app">
    <b-navbar class="dif-font fixed-top nav-config navbar-custom" variant="#000" toggleable="md" type="dark">
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
        <b-navbar-brand href="#inicio">White Wedding Cars</b-navbar-brand>
        <b-collapse is-nav id="nav_collapse">
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item v-for="item in navItems" :key="item.name" :href="item.link">{{ item.name | capitalize }}</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
    </b-navbar>
    <!-- <img src="@/assets/SAL_4921.jpg" fluid alt=""> -->
    <!-- First screen -->
    <div>
      <first-screen-component id="inicio"/>
      <div>
      <sobre-component id="sobre"/>
      <parallax1-component id="parallax1"/>
      <carros-component id="carros"/>
      <parallax2-component/>
      <galeria-component id="galeria"/>
      <parallax3-component/>
      <contato-component id="contato"/>
      <footer-component/>
      </div>
    </div>
  </div>
</template>

<script>
import NavbarComponent from '@/components/Navbar'
import FirstScreenComponent from '@/components/FirstScreen'
import SobreComponent from '@/components/Sobre'
import CarrosComponent from '@/components/Carros'
import Parallax1Component from '@/components/Parallax1'
import Parallax2Component from '@/components/Parallax2'
import GaleriaComponent from '@/components/Galeria'
import Parallax3Component from '@/components/Parallax3'
import ContatoComponent from '@/components/Contato'
import FooterComponent from '@/components//Footer'
export default {
  name: 'App',
  data () {
    return {
      navItems: [
        {name: 'início', link: '#inicio', icon: ''},
        {name: 'sobre', link: '#sobre', icon: ''},
        {name: 'carros', link: '#carros', icon: ''},
        {name: 'galeria', link: '#galeria', icon: ''},
        {name: 'contato', link: '#contato', icon: ''}
      ]
    }
  },
  filters: {
    capitalize: function (value) {
      return value.toUpperCase()
    }
  },
  components: {
    NavbarComponent,
    FirstScreenComponent,
    SobreComponent,
    Parallax1Component,
    CarrosComponent,
    Parallax2Component,
    GaleriaComponent,
    Parallax3Component,
    ContatoComponent,
    FooterComponent
  },
  mounted () {
    $('a').on('click', function (event) {
      if (this.hash !== '') {
        event.preventDefault()
        var hash = this.hash
        $('html, body').animate({
          scrollTop: $(hash).offset().top
        }, 800, function () {
          window.location.hash = hash
        })
      }
    })
  }
}
</script>

<style>
#app {
  font-family: 'Cormorant Garamond', serif;
}
.dif-font {
  font-family: 'Raleway', sans-serif;
}
.navbar-custom {
  background-color: rgba(0, 0, 0);
}
.navbar-dark .navbar-nav .nav-link {
  color: rgba(255, 255, 255);
}
.navbar-dark .navbar-nav .nav-link:hover {
  color: rgba(255, 255, 255, 0.6);
  transition-timing-function: ease-in-out;
  transition: 0.7s;
}
h2, h1 {
  font-family: 'Cormorant Garamond', serif;
  margin: 0;
}
h2 {
  font-size: 36px
}
h1{
  font-size: 124px
}
h3 {
  font-family: 'Cormorant Garamond', serif;
  text-align: center;
  font-size: 72px
}
p{
  font-family: 'Raleway', sans-serif;
}
@media (max-width: 960px) {
  h2 {
    font-size: 30px
  }
  h1 {
    font-size: 72px
  }
}
@media (max-width: 720px) {
  h2 {
    font-size: 24px
  }
  h1 {
    font-size: 62px
  }
}
@media (max-width: 540px) {
  h2 {
    font-size: 22px
  }
  h1 {
    font-size: 44px
  }
}
@media (max-width: 960px) {
  h3 {
    font-size: 48px
  }
  h1 {
    font-size: 72px
  }
}
@media (max-width: 720px) {
  h3 {
    font-size: 40px
  }
  h1 {
    font-size: 62px
  }
}
@media (max-width: 540px) {
  h3 {
    font-size: 32px
  }
  h1 {
    font-size: 44px
  }
}
</style>
