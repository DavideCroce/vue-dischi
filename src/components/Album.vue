<template>
  <div class="album-card">
      <img :src="poster" alt="">
      <h3>{{title}}</h3>
      <p>{{author}}</p>
      <p>{{year}}</p>
  </div>
</template>

<script>
export default {
name: "Album",
props: ["title", "author", "year", "poster"],
}
</script>

<style scoped lang="scss">
.album-card{
    background-color: #2e3a46;
    text-align: center;
    width: 200px;
    height: 350px;
    padding: 20px;
    img{
        width: 150px;
    }
    h3{
        color: white;
        font-size: 20px;
        text-transform: uppercase;
    }
    p{
        color: rgb(117, 117, 117);
    }
}

</style>