<template>
  <div class="disc-container">
      <img :src="infodisccard.poster" :alt="infodisccard.title">
      <h3>{{infodisccard.title}}</h3>
      <h4>{{infodisccard.author}}</h4>
      <h4>{{infodisccard.year}}</h4>
  </div>
</template>

<script>
export default {
    name: 'SingleDiscCard',
    props: {
        'infodisccard': Object
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";

.disc-container{
    width: calc((100% / 5) - 20px);
    margin: 20px 10px;
    padding: 20px;
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