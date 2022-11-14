<script>
import axios from "axios";
export default {
  name: `App`,
  data() {
    return {
      API_URL: `https://www.breakingbadapi.com/api/characters`,
      name: null,
      status: null,
      img: null


    }
  },
  methods: {
    callApi(url) {
      axios.get(url).then(response => {
        console.log(response);
      })
        .catch(err => {
          console.error(err.message);
        })
    }

  },
  mounted() {

  }
}
</script>

<template>

</template>

<style>

</style>
