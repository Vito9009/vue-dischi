<template>
  <div class="selection-container">
        <label>Scegli il genere musicale che preferisci</label>
        <select v-model="genre" :name="genre" @change="$emit('myGenre', genre)">
            <option value="">Ecco tutti i generi disponibili</option>
            <option value="metal">Metal</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>

        </select>
  </div>
</template>

<script>
export default {
    name: 'FilterComponent',

    data() {
        return {
            genre: ""
            }
    }

}
</script>

<style lang="scss" scoped>
@import "../../assets/my_scss/partials/variables.scss";

.selection-container{
    padding: 20px 0;

    label{
        color: rgb(255, 255, 255);
        padding: 0 20px;
        font-weight: bold;
        text-transform: uppercase;
    }

    select{
            width: 250px;
            color: rgb(255, 255, 255);
            background-color: $secondaryColor;
            border: none;
            border-radius: 20px;
            text-align: center;
            padding: 5px 0;
            font-weight: bold;
            text-transform: uppercase;
    }    
}

</style>