<template>
  <TopNavBar/>
  <body>
    <div id="app">
    <div class="content">
      <div class="top-bar">
        <div id="NavigationBar-icon" v-if="mobileView">
          <i class="fa fa-bars"></i>
        </div>
      </div>
    </div>
  </div>
  <router-view
  :baseURL="baseURL"
  :categories="categories"
  :products="products"
  >
  </router-view>
  </body>
  <footer>
    <FooterBar/>
  </footer>
</template>


<script>
import axios from 'axios';
import TopNavBar from './components/sidebar/TopNavBar.vue';
import { sidebarWidth } from './components/sidebar/state';
import FooterBar from './components/FooterBar.vue';
export default {
  components: { TopNavBar, FooterBar },
  setup() {
    return{ sidebarWidth }
  },
  data() {
    return {
      baseURL : "https://api.akilliticaretim.com",
      products: [],
      categories: [],
    }
  },
  methods: {

    async fetchData() {

      // api call to get all the categories
      await axios.get(this.baseURL + "category/")
      .then(res => {
        this.categories = res.data
      }).catch((err) => console.log('err', err));

      // api call to get the products

      await axios.get(this.baseURL + "product/")
      .then(res => {
        this.products = res.data
      }).catch((err) => console.log('err', err));
    }
  },
  mounted() {
    this.fetchData();
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
