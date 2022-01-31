<template>
  <div class="container">
      <div v-if="!loadingDisc" class="row info-disc-list">
        <SingleDiscCard 
        v-for="(element, index) in songInfoArray"
        :key="index"
        :infodisccard="element" 
        class="col-2"/>
      </div>
      
      <Loader v-else />
      
  </div>
</template>

<script>
import axios from "axios";
import SingleDiscCard from "./SingleDiscCard.vue";
import Loader from "../Loader/Loader.vue";

export default {
    name: 'SongsCardsComponent',
    components: {
        SingleDiscCard,
        Loader
    },
    data(){
        return{
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            songInfoArray: [],
            loadingDisc: false
        }
    },
    methods: {
        getDiscCard(){
            axios.get(this.apiUrl)
                .then((response) => {
                    
                    this.songInfoArray = response.data.response;

                })
                .catch(function (error) {
                    
                    console.log(error);
                });
        }
    },
    created(){
        this.getDiscCard();
    }

}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";

</style>