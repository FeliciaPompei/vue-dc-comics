<template>
  <div>
    <div class="bg-gray">
      <div class="main-content">
        <h1> Content goes here </h1>
    </div>
    <div class="bg-blue">
      <div class="main-content">
        <ul>
          <li>
            <img src="../assets/img/buy-comics-digital-comics.png" alt="DC digital comics">
            <a href="#">digital comics</a>
          </li>
          <li>
            <img src="../assets/img/buy-comics-merchandise.png" alt="DC merchandise">
            <a href="#">dc merchamdise</a>
          </li>
          <li>
            <img src="../assets/img/buy-comics-subscriptions.png" alt="DC subscriptions">
            <a href="#">subscription</a>
          </li>
          <li>
            <img src="../assets/img/buy-comics-shop-locator.png" alt="DC digital shop locator">
            <a href="#">comic shop locator</a>
          </li>
          <li>
            <img src="../assets/img/buy-dc-power-visa.svg" alt="DC power visa">
            <a href="#">dc power visa</a>
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
  justify-content: space-evenly;
  align-items: center;
  height: 20vh;
  width: 70%;
  margin: 0 auto;

  h1 {
    color:white;
  }

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
