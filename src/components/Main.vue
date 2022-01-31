<template>
  <div class="container">
    <div class="my_main-container">
        <MainComponents />
    </div>
  </div>
</template>

<script>
import MainComponents from "./MainComponents/MainComponents.vue"

export default {
    name: 'Main',
    components: {
      MainComponents
    }

}
</script>

<style lang="scss" scoped>


</style>