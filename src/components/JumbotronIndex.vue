<template>
    <div id="my-jumbotron">
    </div>
</template>

<script>
export default {
  name: 'ComicCard',
  props: ['comicCard']
}
</script>


<style scoped lang="scss">

#my-jumbotron{
  height:35vh;
  width:100%;
  background-image: url(../assets/img/jumbotron.jpg);
  background-size:cover;
}

</style>
