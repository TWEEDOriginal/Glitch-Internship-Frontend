<template>
  <div id="app">
    
   <AquilaAveion :details="details"/>
  </div>
</template>

<script>

import AquilaAveion from './components/AquilaAveion'
export default {
  name: 'App',
  components: {
    AquilaAveion
  },
  mounted: function () {
   window.axios.get('https://hirng-x2021.glitch.me/api')
   .then(res => this.details = res.data)
   .catch(err => console.log(err))
  },
  data: function () {
  return{
    details: {
      name: null,
      social_media : {
        instagram: null,
        twitter: null,
        snapchat: null,
        email: null,
      },
    }
  }
    }
  
}
</script>

<style>
   * {
     box-sizing: border-box;
     margin: 0;
     padding: 0;
   }

   body {
     font-family: Arial, Helvetica, sans-serif;
     line-height: 1.4;
     color:white;
   }
</style>
