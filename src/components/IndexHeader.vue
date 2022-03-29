<template>
  <div id="main-header">
    <div id="header-wrapper" class="my-flex my-container">
      <img class="my-height-100" src="../assets/img/dc-logo.png" alt="DC logo">
      <ul class="my-flex my-height-100">
        <li class="my-height-100" v-for="(link,index) in headerLinks" :key="index" :class="{active: link.active}" @click="activeLink(index)">
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
  methods : {
    activeLink(baseIndex){
      this.headerLinks.forEach((element, index) => {
          if (baseIndex === index ){
              element.active = true;
          } else {
              element.active = false;
          }
      });
    }
  }
}
</script>


<style scoped lang="scss">
@import "../assets/scss/style.scss";

#header-wrapper{
  justify-content: space-between;
  align-items:center;
  height: 10vh;

  img{
    padding: 0.5rem;
  }

  ul{
    align-items: center;

    li{
        padding: 0.4rem;
        font-size: 0.8rem;
        line-height:9vh;
        
      a{
        text-transform: uppercase;
        color: $blackColor;
      }

      &:active,
      .active {
        border-bottom: 5px solid $primaryColor;
      }
    }
  }
  
}
</style>
