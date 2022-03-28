<template>
  <div id="main-header">
    <div id="header-wrapper">
      <img src="../assets/img/dc-logo.png" alt="DC logo">
      <ul>
        <li>
          <a href="#">characters</a>
        </li>
        <li>
          <a href="#">comics</a>
        </li>
        <li>
          <a href="#">movies</a>
        </li>
        <li>
          <a href="#">tv</a>
        </li>
        <li>
          <a href="#">games</a>
        </li>
        <li>
          <a href="#">collectibles</a>
        </li>
        <li>
          <a href="#">videos</a>
        </li>
        <li>
          <a href="#">fans</a>
        </li>
        <li>
          <a href="#">news</a>
        </li>
        <li>
          <a href="#">shop</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexHeader',
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
    padding: 1rem;
    font-size: 0.7rem;


    a{
      text-decoration: none;
      text-transform: uppercase;
      color:black;
    }
  }
}


</style>
