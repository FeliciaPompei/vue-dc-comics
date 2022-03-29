<template>
  <div id="main-footer">
    <div id="top-footer">
      <div class="top-footer-wrapper">
        <div class="footer-nav-bar">
        <ul>
          <li>dc comics</li>
          <li v-for="(link, index) in dcComicsLinks" :key="index">
            <a :href="link.link"> {{link.text}} </a>
          </li>
        </ul>
        <ul>
          <li>dc</li>
          <li><a href="#">Item</a></li>
          <li v-for="(link, index) in dcLinks" :key="index">
            <a :href="link.link"> {{link.text}} </a>
          </li>
        </ul>
        <ul>
          <li>sites</li>
          <li v-for="(link, index) in dcSiteLinks" :key="index">
            <a :href="link.link"> {{link.text}} </a>
          </li>
        </ul>
        <ul>
          <li>shop</li>
          <li v-for="(link, index) in dcShopLinks" :key="index">
            <a :href="link.link"> {{link.text}} </a>
          </li>
        </ul>
      </div>
      <img src="../assets/img/dc-logo-bg.png" alt="DC Logo">
      </div>
    </div>
    <div class="bottom-footer">
      <div class="bottom-footer-wrapper">
        <div class="btn">
          <a href="#">sign-up Now!</a>
        </div>
        <div class="social-media">
          <h4>follow us</h4>
          <a :href="link.link" v-for="(link, index) in socialMediaLinks" :key="index">
            <img :src="link.image" :alt="link.text">
          </a>
        </div>

      </div>
    </div>  
  </div>
</template>

<script>
export default {
  name: 'IndexFooter',
  data(){
    return{
      dcComicsLinks : [
        {
          text: 'Characters',
          link: '#'
        },
        {
          text: 'Comics',
          link: '#'
        },
        {
          text: 'movies',
          link: '#'
        },
        {
          text: 'TV',
          link: '#'
        },
        {
          text: 'Games',
          link: '#'
        },
        {
          text: 'Videos',
          link: '#'
        },
        {
          text: 'News',
          link: '#'
        }
      ],
      dcLinks : [
        {
          text: 'Terms Of Use',
          link: '#'
        },
        {
          text: 'Privacy policy (New)',
          link: '#'
        },
        {
          text: 'Ad Choices',
          link: '#'
        },
        {
          text: 'Advertising',
          link: '#'
        },
        {
          text: 'Jobs',
          link: '#'
        },
        {
          text: 'Subscriptions',
          link: '#'
        },
        {
          text: 'Talent Workshop',
          link: '#'
        },
        {
          text: 'CPSC Certificates',
          link: '#'
        },
        {
          text: 'Rating',
          link: '#'
        },
        {
          text: 'Shop Help',
          link: '#'
        },
        {
          text: 'Contact Us',
          link: '#'
        }
      ],
      dcSiteLinks : [
        {
          text: 'DC',
          link: '#'
        },
        {
          text: 'MAD Magazine',
          link: '#'
        },
        {
          text: 'DC Kids',
          link: '#'
        },
        {
          text: 'DC Universe',
          link: '#'
        },
        {
          text: 'DC Power Visa',
          link: '#'
        }
      ],
      dcShopLinks : [
        {
          text: 'Shop DC',
          link: '#'
        },
        {
          text: 'Shop DC Collectibles',
          link: '#'
        }
      ],
      socialMediaLinks : [
        {
          text:'Facebook logo',
          image: './img/footer-facebook.png',
          link: '#'
        },
        {
          text:'Twitter logo',
          image: './img/footer-twitter.png',
          link: '#'
        },
        {
          text:'Youtube logo',
          image: './img/footer-youtube.png',
          link: '#'
        },
        {
          text:'Pinterest logo',
          image: './img/footer-pinterest.png',
          link: '#'
        },
        {
          text:'Periscope logo',
          image: './img/footer-periscope.png',
          link: '#'
        }

      ]
    }
  }
}
</script>


<style scoped lang="scss">
@import "../assets/scss/style.scss";

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
    width:30%;

    ul{
      margin: 0.8rem;
      li{
        list-style: none;
        color:white;
        text-transform: uppercase;
        font-size:0.8rem;

        a{
          text-decoration: none;
          color:lightgray;
          text-transform: lowercase;
          font-size: 0.7rem;
        }
      }
    }
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

        h4{
          color: #0282f9;
          text-transform: uppercase;
          margin-right: 0.5rem;
        }
        img{
          margin: 0.5rem;
        }
      }
      .btn {
        border: 2px solid #0282f9;
        padding: 0.5rem;
        a{
        text-decoration: none;
        text-transform: uppercase;
        color:white;
        
        padding: 0.5rem;
      }
      }
  }
}
</style>
