<template>
  <div>
    <div class="bg-gray">
      <div class="main-content">
        <h3> Content goes here </h3>
    </div>
    <div class="bg-blue">
      <div class="nav-wrapper">
        <ul>
          <li v-for="(link, index) in dcStore" :key="index">
            <img :src="link.image" :alt="link.text">
            <a :href="link.link"> {{link.text}} </a>
          </li>
        </ul>
    </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexMain',
  data(){
    return {
      dcStore : [
        {
          text: 'digital comics',
          image: './img/buy-comics-digital-comics.png',
          link : '#'
        },
        {
          text: 'dc merchamdise',
          image: './img/buy-comics-merchandise.png',
          link : '#'
        },
        {
          text: 'subscription',
          image: './img/buy-comics-subscriptions.png',
          link : '#'
        },
        {
          text: 'comic shop locator',
          image: './img/buy-comics-shop-locator.png',
          link : '#'
        },
        {
          text: 'dc power visa',
          image: './img/buy-dc-power-visa.svg',
          link : '#'
        }
      ],
    }
  }
}
</script>


<style scoped lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.bg-gray{
  background-color:#1c1c1c;
}

.main-content{
  display: flex;
  align-items: center;
  height: 20vh;
  width: 70%;
  margin: 0 auto;

  h3 {
    color:white;
  }
}

.nav-wrapper{
  display: flex;
  align-items: center;
  height: 20vh;
  width: 70%;
  margin: 0 auto;

  ul{
    display:flex;
    justify-content: center;
    width:100%;

    li{
    list-style: none;
    display: inline;

      img{
        width:20%;
        vertical-align: middle;
        margin-right: 0.2rem;
        
      }

      a {
        text-decoration: none;
        text-transform: uppercase;
        color:white;
        font-size: 0.5rem;
      }
    }
  }
}

.bg-blue{
  background-color:#0282f9;
}

</style>
