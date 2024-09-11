<script>
  export default {
  data() {
    return { 
      mainLinks: [
      {
          label: 'digital comics',
          icon:'src/assets/img/buy-comics-digital-comics.png',
          url: '#',
          active: false
        },
        {
          label: 'dc merchandise',
          icon:'src/assets/img/buy-comics-merchandise.png',
          url: '#',
          active: false
        },
        {
          label: 'subscription',
          icon:'src/assets/img/buy-comics-subscriptions.png',
          url: '#',
          active: false
        },
        {
          label: 'comic shop locator',
          icon:'src/assets/img/buy-comics-shop-locator.png',
          url: '#',
          active: false
        },
        {
          label: 'dc power visa',
          icon:'src/assets/img/buy-dc-power-visa.svg',
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
                <!-- :src="link.icon" non funziona perchè? con percorso assoluto funziona--chiedere -->
                <img :src="link.icon" :alt="link.label">
                {{ link.label }}
              </a>
            </li>
            
          </ul>
        </div>
      </div>

    </main>
</template>

<style lang="scss" scoped>
  p {
  color:white;
  padding: 50px 0;
  font-weight: bold;
  font-size: 1.5rem;

}
.main-bottom {
  background-color: #0C7CEC;
  ul {
    list-style: none;
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-around;
    align-items: center;
    padding: 0;
      li {
        padding: 50px 0;
        
        a {
          text-decoration: none;
          color: white;
          text-transform: uppercase;
          font-weight: bold;
          font-size: 1.1rem;
          display: flex;
          align-items: center;
            img {
              margin-right: 15px;
              width: 40px;

            }
        }
      }
  }
}

</style>
