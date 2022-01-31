<template>
  <div class="header-container">
      <div class="logo-container">
          <img src="https://cantabrialabsdifacooper.it/wp-content/uploads/2021/03/png-clipart-spotify-logo-spotify-computer-icons-podcast-music-apps-miscellaneous-angle-1-e1614848134495-300x300.png" alt="">
      </div>
  </div>
</template>

<script>
export default {
    name: 'HeaderComponents'

}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";


.header-container{
    width: 100%;
    height: 80px;
    background-color: $secondaryColor;
    display: flex;
    align-items: center;
    
    .logo-container{
        width: 10%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;

        img{
            width: 60px;
        }

    }
}
</style>