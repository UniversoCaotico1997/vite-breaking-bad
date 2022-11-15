<script>
import { store } from "./assets/js/store";
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
export default {
  name: `App`,
  components: {
    AppHeader,
    AppMain
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

  <AppHeader></AppHeader>

  <AppMain></AppMain>

</template>

<style lang="scss" scoped>

</style>
