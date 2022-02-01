<template>
  <div>
      <header>
          <HeaderComponents />
      </header>
  </div>
</template>

<script>
import HeaderComponents from "./HeaderComponents/HeaderComponents.vue"


export default {
    name: 'Header',
    components: {
        HeaderComponents
    }

}
</script>

<style lang="scss" scoped>
header{
    position: fixed;
    top: 0;
    width: 100%;
}

</style>