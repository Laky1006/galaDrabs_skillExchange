<template>
  <main>
    <p>
      Times clicked: {{score}}
    </p>
    <div>
      <img src="https://captaincookiedc.com/wp-content/uploads/2023/04/home-icon-cookie.png" 
      @click="handleClickEvent">
    </div>
  </main>
</template>


<script>
  export default {
    data(){
      return {
        score: 0,
      }
    },
    methods: {
      handleClickEvent(){
        this.score++
      }
    }
  }
</script>


<style scoped>
  img {
    height: 500px;
  }

  div {
    height: 94vh;
    width: 98vw;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>