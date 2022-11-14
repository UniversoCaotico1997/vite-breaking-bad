<script>
// import AppHeader from "./components/AppHeader.vue";
import { store } from "./assets/js/store";
import axios from "axios";
export default {
  name: `App`,
  components: {
    // AppHeader
  },
  data() {
    return {
      store,
    }
  },
  methods: {
    callApi(url) {
      axios.get(url).then(response => {
        console.log(response);
        this.store.characters = response.data
        console.log(this.store.characters);
      })
    }

  },
  mounted() {
    this.callApi(this.store.API_URL)
  }
}
</script>

<template>

  <h1>Breaking bad Api</h1>
  <div class="container">
    <div class="characters"></div>
    <div class="row row-cols-5">
      <div class="col" v-for="item in store.characters">
        <div class="card">
          <img :src="item.img" class="card-img-top" alt="">
          <div class="card-body">
            <h5 class="card-title">{{ item.name }} </h5>
            <p class="card-text">{{ item.status }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>

</style>
