<template>
  <div>
    <main>
      <SongsCardsComponent />
    </main>     
  </div>
</template>

<script>
import SongsCardsComponent from "./SongsCardsComponent.vue"

export default {
    name: 'MainComponents',
    components: {
      SongsCardsComponent
    }

}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";

main {
  margin: 100px;
}
</style>