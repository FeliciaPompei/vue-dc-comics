<template>
  <div id="main-header">
    <div id="header-wrapper">
      <img src="../assets/img/dc-logo.png" alt="DC logo">
      <ul>
        <li v-for="(link,index) in headerLinks" :key="index" :class="(headerLinks.active) ? 'active' : ''">
          <a :href="link.link"> {{link.text}} </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexHeader',
  data(){
    return{
      headerLinks : [
        {
          text: 'characters',
          link: '#',
          active: false,
        },
        {
          text: 'comics',
          link: '#',
          active: true,
        },
        {
          text: 'movies',
          link: '#',
          active: false,
        },
        {
          text: 'tv',
          link: '#',
          active: false,
        },
        {
          text: 'games',
          link: '#',
          active: false,
        },
        {
          text: 'collectibles',
          link: '#',
          active: false,
        },
        {
          text: 'videos',
          link: '#',
          active: false,
        },
        {
          text: 'fans',
          link: '#',
          active: false,
        },
        {
          text: 'news',
          link: '#',
          active: false,
        },
        {
          text: 'shop',
          link: '#',
          active: false,
        },
      ],
    }
  },
}
</script>


<style scoped lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#header-wrapper{
  display: flex;
  justify-content: space-between;
  align-items:center;
  height: 20vh;
  width: 70%;
  margin: 0 auto;

  img{
    height:55%;
  }

  li{
    list-style: none;
    display: inline;
    padding: 0.4rem;
    font-size: 0.7rem;


    a{
      text-decoration: none;
      text-transform: uppercase;
      color:black;
    }

    &:active,
    .active {
      color:#0282f9;
      border-bottom: 3px solid #0282f9;
    }
  }
}


</style>
