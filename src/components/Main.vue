<template>
  <div class="main">
      <div class="cards-container" >
          <Album v-for="card in cards" :key="card"
          :author="card.author"
          :title="card.title"
          :year="card.year"
          :poster="card.poster"
          />
      </div>
  </div>
</template>

<script>
import axios from "axios";
import Album from "./Album.vue";
export default {
name: 'Main',
components:{
    Album,
},
data() {
    return{
        cards:[],
    }
},
mounted(){
    axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {
        this.cards = res.data.response
    });
},
}

</script>

<style scoped lang="scss">
.main{
    background-color: #1e2d3b;
    height: 100vh;
    width: 100%;
    padding-top: 100px;
    .cards-container{
        width: 1000px;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
    }
}
</style>