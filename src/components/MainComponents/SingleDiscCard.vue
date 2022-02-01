<template>
  <div class="disc-container">
      <img :src="infoDiscCard.poster" :alt="infoDiscCard.title">
      <h3>{{infoDiscCard.title}}</h3>
      <h4>{{infoDiscCard.author}}</h4>
      <h4>{{infoDiscCard.year}}</h4>
  </div>
</template>

<script>
export default {
    name: 'SingleDiscCard',
    props: {
        'infoDiscCard': Object
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";

.disc-container{
    width: calc((100% / 5) - 20px);
    margin: 20px 10px;
    padding: 10px;
    text-align: center;
    background-color: $secondaryColor;

    h3{
        color: rgb(255, 255, 255);
        text-transform: uppercase;
        font-weight: bold;
        margin-bottom: 20px
        
    }

    h4{
        color: $singerInfoColor;

    }

    img{
        width: 100%;
        margin-bottom: 20px;
    }
}

</style>