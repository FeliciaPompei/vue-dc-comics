<template>
    <div class="my-card my-flex">
      <div class="my-card-img">
        <img :src="comicCard.thumb" :alt="comicCard.series">
      </div>
      <div>
        <h4> {{comicCard.series}} </h4>
        <p> {{comicCard.price}} </p>
      </div>
    
    </div>
</template>

<script>
export default {
  name: 'ComicCard',
  props: ['comicCard']
}
</script>


<style scoped lang="scss">
@import "../assets/scss/style.scss";

.my-card{
  width:140px;
  height:180px;
  flex-wrap: wrap;
  margin: 0.2rem 0.2rem 2rem;

  h4, p{
    text-align:left;
    color:white;
  }
}
  .my-card-img{
    width: 120px;
    height:120px;

    img{
      width:100%;
      height:100%;
      margin-bottom:0.5rem;
    }
  }

</style>
