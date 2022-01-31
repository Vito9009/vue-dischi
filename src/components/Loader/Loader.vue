<template>
  <div class="loader-container">
      <div class="loader">
          <h3>Sto caricando...</h3>
          <img src="https://cantabrialabsdifacooper.it/wp-content/uploads/2021/03/png-clipart-spotify-logo-spotify-computer-icons-podcast-music-apps-miscellaneous-angle-1-e1614848134495-300x300.png" alt="">

      </div>
  </div>
</template>

<script>
export default {
    name: 'Loader'
}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";

.loader-container{
    display: flex;
    justify-content: center;
    align-items: center;

    .loader {
    text-align: center;
    color: rgb(255, 255, 255);

    img{
        width: 100px;
    }
}

}

</style>