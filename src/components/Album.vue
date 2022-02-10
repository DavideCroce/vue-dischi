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
    width: 180px;
    height: 325px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    flex-direction: column;
    padding-top: 15px;
    img{
        width: 150px;
        margin-bottom: 20px;
    }
    h3{
        color: white;
        font-size: 20px;
        text-transform: uppercase;
        padding-bottom: 20px;
    }
    p{
        color: rgb(117, 117, 117);
    }
}

</style>