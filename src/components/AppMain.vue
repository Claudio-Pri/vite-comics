<script>
  export default {
  data() {
    return { 
      mainLinks: [
      {
          label: 'digital comics',
          icon:'../assets/img/buy-comics-digital-comics.png',
          url: '#',
          active: false
        },
        {
          label: 'dc merchandise',
          icon:'../assets/img/buy-comics-merchandise.png',
          url: '#',
          active: false
        },
        {
          label: 'subscription',
          icon:'../assets/img/buy-comics-subscription.png',
          url: '#',
          active: false
        },
        {
          label: 'comic shop locator',
          icon:'../assets/img/buy-comics-shop-locator.png',
          url: '#',
          active: false
        },
        {
          label: 'dc power visa',
          icon:'../assets/img/buy-dc-power-visa.svg',
          url: '#',
          active: false
        },
      ]
     }
  },
}
</script>

<template>
  <main>
      <div class="container">
        <p>
          --&gt;Content Goes Here &lt;--
        </p>
      </div>
      <div class="main-bottom">
        <div class="container">
          <ul>
            <li v-for="(link, index) in mainLinks" :key="index">
              <a href="#">
                <!-- :src="link.icon" non funziona perchè? -->
                <img :src="link.icon" :alt="link.label">
                {{ link.label }}
              </a>
            </li>
            
          </ul>
        </div>
      </div>

    </main>
</template>

<style scoped>
  p {
  color:white;
  padding: 50px 0;
  font-weight: bold;
  font-size: 1.5rem;

}
.main-bottom {
  background-color: #0C7CEC;
}

ul {
  list-style: none;
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-around;
  padding: 0;
}

ul li {
  padding: 50px 0;
  
}

ul li a {
  text-decoration: none;
  color: white;
  text-transform: uppercase;
  font-weight: bold;
  font-size: 1.1rem;
  display: flex;
  align-items: center;
  

}
ul li a img {
  margin-right: 15px;
  width: 60px;

}





</style>
