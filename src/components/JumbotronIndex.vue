<template>
    <div id="my-jumbotron">
    </div>
</template>

<script>
export default {
  name: 'JumbotronIndex',
}
</script>


<style scoped lang="scss">
@import "../assets/scss/style.scss";
#my-jumbotron{
  height:35vh;
  width:100%;
  background-image: url(../assets/img/jumbotron.jpg);
  background-size:cover;
}
</style>
