<template>
  <div id="main-footer">
    <div id="top-footer">
      <div class="top-footer-wrapper">
        <div class="footer-nav-bar">
        <ul>
          <li>dc comics</li>
          <li><a href="#">Item</a></li>
        </ul>
        <ul>
          <li>dc</li>
          <li><a href="#">Item</a></li>
        </ul>
        <ul>
          <li>sites</li>
          <li><a href="#">Item</a></li>
        </ul>
        <ul>
          <li>shop</li>
          <li><a href="#">Item</a></li>
        </ul>
      </div>
      <img src="../assets/img/dc-logo-bg.png" alt="DC Logo">
      </div>
    </div>
    <div class="bottom-footer">
      <div class="bottom-footer-wrapper">
        <a href="#">sign-up Now!</a>
        <div class="social-media">
          <h4>follow us</h4>
          <img src="../assets/img/footer-facebook.png" alt="">
          <img src="../assets/img/footer-twitter.png" alt="">
          <img src="../assets/img/footer-youtube.png" alt="">
          <img src="../assets/img/footer-pinterest.png" alt="">
          <img src="../assets/img/footer-periscope.png" alt="">
        </div>

      </div>
    </div>  
  </div>
</template>

<script>
export default {
  name: 'IndexFooter',
}
</script>


<style scoped lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#top-footer{
  height: 40vh;
  background-image: url(../assets/img/footer-bg.jpg);
  background-size:cover;
}

.top-footer-wrapper{
  width:70%;
  height:40vh;
  margin: 0 auto;
  display:flex;
  justify-content: space-between;
  overflow: hidden;

  .footer-nav-bar{
    display:flex;
    flex-wrap: wrap;
    width:50%;

    ul{
      margin: 2rem;
      li{
        list-style: none;
        color:white;

        a{
          text-decoration: none;
          text-transform: uppercase;
          color:white
        }
      }
    }
  }
  img {
    // height:150%;
  }
}

.bottom-footer{
  background-color: #303030;
  height: 10vh;

  .bottom-footer-wrapper{
      display:flex;
      justify-content:space-between;
      width:70%;
      height:100%;
      margin: 0 auto;
      align-items: center;

      .social-media{
        display:flex;
        align-items: center;
      }
  }
}
</style>
