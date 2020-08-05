

<template>
  <div class="home">
    <h1>{{ message }}</h1>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!"
    };
  },
  created: function() {
    this.indexContacts();
  },
  methods: {
    indexContacts: function() {
      console.log('contacts index');
      axios.get('/api/contacts').then(response => {
        console.log(response.data)
      })
    }
  }
};
</script>
