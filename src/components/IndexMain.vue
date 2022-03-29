<template>
  <div>
    <div class="bg-gray">
      <JumbotronIndex />
      <div class="main-content my-flex my-container">
        <a class="btn btn-position" href="#">current series</a>
        <ComicCard
        v-for="(card, index) in dcCards" 
        :key="index"
        :comicCard ="card"
        />
        <a class="btn">Load More</a>
      
      </div>
    </div>
    <div class="bg-blue">
      <ShoppingNav/>
    </div>
  </div>
</template>

<script>
import ComicCard from './ComicCard.vue'
import JumbotronIndex from './JumbotronIndex.vue'
import ShoppingNav from './ShoppingNav.vue'

export default {
  name: 'IndexMain',
  components: {
    ComicCard,
    JumbotronIndex,
    ShoppingNav
  },
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
      dcCards : [
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel"
        }
      ],
    }
  }
}
</script>


<style lang="scss">
@import "../assets/scss/style.scss";

.bg-gray{
  background-color: $darkGray;
}

.main-content{
  flex-wrap: wrap;
  align-items: center;
  padding: 2rem;
  justify-content: center;
  position:relative;
}

.bg-blue{
  background-color:$primaryColor;
}

.btn {
  background-color: $primaryColor;
  padding: 0.5rem 3rem;
  color:white;
  text-align:center;
  text-transform: uppercase;
  font-size:0.8rem;
}

.btn-position{
  position:absolute;
  top:-15px;
  left: 15px;
  padding: 0.5rem 1rem;
  font-size: 1rem;

}

</style>
