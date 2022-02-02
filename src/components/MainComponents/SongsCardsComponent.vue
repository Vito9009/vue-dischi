<template>
<div>
  <div v-if="valueGenre!=''" class="container my_option-container">
      <div class="my_option-container">
          <FilterComponent @myGenre="genresFilter" />
      </div>
      <div v-if="!loadingDisc" class="row info-disc-list">
        <SingleDiscCard 
        v-for="(element, index) in valueGenreFilter"
        :key="index"
        :info-disc-card="element" 
        class="col-2"/>
      </div>
  </div>


  <div v-else class="container">
      <div class="my_option-container">
          <FilterComponent @myGenre="genresFilter" />
      </div>
      <div v-if="!loadingDisc" class="row info-disc-list">
        <SingleDiscCard 
        v-for="(element, index) in songInfoArray"
        :key="index"
        :info-disc-card="element" 
        class="col-2"/>
      </div>
      
      <Loader v-else />
  </div>
</div>
</template>

<script>
import axios from "axios";
import SingleDiscCard from "./SingleDiscCard.vue";
import Loader from "../Loader/Loader.vue";
import FilterComponent from "../FilterComponent/FilterComponent.vue";


export default {
    name: 'SongsCardsComponent',
    components: {
        SingleDiscCard,
        Loader,
        FilterComponent
    },
    data(){
        return{
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            songInfoArray: [],
            loadingDisc: false,
            valueGenre: ""
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
        },
        genresFilter: function(elementGenre) {
            this.valueGenre = elementGenre;
        }
    },
    created(){
        this.getDiscCard();
    },
    computed: {
        valueGenreFilter() {
            return this.songInfoArray.filter(element =>
            element.genre.toLowerCase() == this.valueGenre.toLowerCase()
            )
        }
    }

}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";

.my_option-container{
    text-align: center;
}
</style>