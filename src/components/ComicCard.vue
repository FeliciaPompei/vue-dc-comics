<template>
    <div class="my-card">
      <img :src="comicCard.thumb" alt="">
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

  .my-card{
    width: calc(80% / 6);
    background-color: white;
    display: flex;
    flex-wrap:wrap;
    justify-content: center;
    align-items: center;;
    padding:0.5rem;
    align-content: center;
    margin: 0.5rem;
    font-size: 0.8rem;
    img{
      width:50%;
    }
  }

</style>
