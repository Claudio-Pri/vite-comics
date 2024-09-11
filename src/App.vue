<script>
/*
Passaggi import componente:
1) Importazione componente
2) Dichiarazione del componente
3) Utilizzo del componente
*/

// 1) Importazione componente
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

  export default {
  data() {
    return { 
      footerLinks: [
        {
          label: 'characters',
          url: '#',
          active: false
        },
        {
          label: 'comics',
          url: '#',
          active: false
        },
        {
          label: 'movies',
          url: '#',
          active: false
        },
        {
          label: 'tv',
          url: '#',
          active: false
        },
        {
          label: 'games',
          url: '#',
          active: false
        },
        {
          label: 'collectibles',
          url: '#',
          active: false
        },
        {
          label: 'videos',
          url: '#',
          active: false
        },
        {
          label: 'fans',
          url: '#',
          active: false
        },
        {
          label: 'news',
          url: '#',
          active: false
        },
        
      ],
      footerShopLinks: [
        {
          label: 'shop dc',
          url: '#',
          active: false
        },
        {
          label: 'shop dc collectibles',
          url: '#',
          active: false
        }
      ],
      footerDcLinks: [
        {
          label: 'terms of use',
          url: '#',
          active: false
        },
        {
          label: 'privacu policy (new)',
          url: '#',
          active: false
        },
        {
          label: 'ad choiches',
          url: '#',
          active: false
        },
        {
          label: 'advertising',
          url: '#',
          active: false
        },
        {
          label: 'jobs',
          url: '#',
          active: false
        },
        {
          label: 'subscriptions',
          url: '#',
          active: false
        },
        {
          label: 'talent workshops',
          url: '#',
          active: false
        },
        {
          label: 'cpsc certificates',
          url: '#',
          active: false
        },
        {
          label: 'ratings',
          url: '#',
          active: false
        },
        {
          label: 'shop help',
          url: '#',
          active: false
        },
        {
          label: 'contact us',
          url: '#',
          active: false
        },
      ],
      footerSitesLinks: [
        {
          label: 'dc',
          url: '#',
          active: false
        },
        {
          label: 'mad magazine',
          url: '#',
          active: false
        },
        {
          label: 'dc kids',
          url: '#',
          active: false
        },
        {
          label: 'dc universe',
          url: '#',
          active: false
        },
        {
          label: 'dcpower visa',
          url: '#',
          active: false
        },
      ],
     }
  },
  //2) Dichiarazione del componente (prima o dopo data())
  components: {
    AppHeader,
    AppMain,
  },
  methods: {
    
  }
}
</script>

<template>
  <!-- N.B. Template vuole 1 solo figlio -->
  <div>
    <!-- 3) Utilizzo del componente come tag htm (self-closing) -->
    <AppHeader/>

    <AppMain/>
    
    
    <footer>
      <div class="footer-top">
        <div class="container">
          <div class="row">
            <div class="col-50">
              <div class="footer-nav">
                <div class="row">
                  <div class="col-33">
                    <h4>dc comics</h4>
                    <ul>
                      <li v-for="(link, index) in footerLinks" :key="index">
                        <a href="#">{{ link.label }}</a>
                      </li>
                    </ul>
                    <h4>shop</h4>
                    <ul>
                      <li v-for="(link, index) in footerShopLinks" :key="index">
                        <a href="#">{{ link.label }}</a>
                      </li>
                    </ul>
                  </div>
                  <div class="col-33">
                    <h4>dc</h4>
                    <ul>
                      <li v-for="(link, index) in footerDcLinks" :key="index">
                        <a href="#">{{ link.label }}</a>
                      </li>
                    </ul>
                  </div>
                  <div class="col-33">
                    <h4>dc</h4>
                    <ul>
                      <li v-for="(link, index) in footerSitesLinks" :key="index">
                        <a href="#">{{ link.label }}</a>
                      </li>
                    </ul>
                  </div>
                </div>
                
              </div>
            </div>
            <div class="col-50 bg-logo"></div>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="container">
          footer bottom
        </div>
      </div>
    </footer>
    
  </div>
</template>

<style lang="scss" scoped>
// npm add -d sass
// @use 'assets/scss/main.scss' as *;
// @use 'assets/scss/variables.scss' as *;
footer {
  color: white;
}
h4 {
  text-transform: uppercase;
  padding: 15px 0;
}
ul {
  list-style: none;
  padding: 0;
}
ul li {
  padding: 3px 0;
}
ul li a {
  text-decoration: none;
  text-transform: capitalize;
  color: white;

}
.footer-top {
  background-image: url(/src/assets/img/footer-bg.jpg);
  background-position: center;
  background-size: cover;
}
.bg-logo {
  background-image: url(/src/assets/img/dc-logo-bg.png);
  background-position: center;
  background-size:cover;
}


</style>
