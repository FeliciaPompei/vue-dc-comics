<template>
  <nav class="nav-wrapper my-flex my-container">
      <ul class="my-flex">
        <li v-for="(link, index) in dcStore" :key="index">
          <img :src="link.image" :alt="link.text">
          <a :href="link.link"> {{link.text}} </a>
        </li>
      </ul>
  </nav>
</template>

<script>
export default {
  name: 'ComicCard',
  // props: [''] TO CHANGE
}
</script>


<style scoped lang="scss">
@import "../assets/scss/style.scss";
.nav-wrapper{
  align-items: center;
  height: 20vh;

  ul{
    justify-content: center;
    width:100%;

    li{
      img{
        width:20%;
        vertical-align: middle;
        margin-right: 0.2rem;
        
      }

      a {
        text-transform: uppercase;
        color:white;
        font-size: 0.5rem;
      }
    }
  }
}
</style>
