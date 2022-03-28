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
          image: '../../assets/img/buy-comics-digital-comics.png',
          link : '#'
        },
        {
          text: 'dc merchamdise',
          image: '../assets/img/buy-comics-merchandise.png',
          link : '#'
        },
        {
          text: 'subscription',
          image: '../assets/img/buy-comics-subscriptions.png',
          link : '#'
        },
        {
          text: 'comic shop locator',
          image: '../assets/img/buy-comics-shop-locator.png',
          link : '#'
        },
        {
          text: 'dc power visa',
          image: '../assets/img/buy-dc-power-visa.svg',
          link : '#'
        }
      ],
    }
  }
}
</script>


<style scoped lang="scss">
*{
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
  justify-content: space-evenly;
  height: 20vh;
  width: 70%;
  margin: 0 auto;
    li{
    list-style: none;
    display: inline;
    margin:1rem;

  img{
    width:5%;
    vertical-align: middle;
    margin-right: 0.4rem;
    
  }

    a {
      text-decoration: none;
      text-transform: uppercase;
      color:white;
      font-size: 0.5rem;
    }
  }
}

.bg-blue{
  background-color:#0282f9;
}

</style>
