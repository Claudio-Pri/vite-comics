<script>
  export default {
  data() {
    return { 
      headerLinks: [
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
        {
          label: 'shop',
          url: '#',
          active: false
        },
      ]
     }
  },
}
</script>

<template>
  <header>
      <div class="container">
        <div class="my-header">
          <div>
            <a href="#">
              <img src="../assets/img/dc-logo.png" alt="DC Logo">
            </a>
          </div>
          <nav>
            <ul>
              <li v-for="(link, index) in headerLinks" :key="index">
                <a href="#">{{ link.label }}</a>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </header>
</template>

<style scoped>

header {
padding: 30px 0;
background-color: white;
margin-top: 10px;
}
.my-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
ul {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  padding: 0;
}
ul li {
  margin-right: 15px;
}
ul li a {
  display: inline-block;
  text-decoration: none;
  text-align: right;
  text-transform: uppercase;
  color:#4C4D4A;
  font-weight: bold;
}
ul li a:hover {
  color:#0C7CEC;
 
}

</style>
