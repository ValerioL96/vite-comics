<script >
export default{
  data() {
    return{
      comicsList:[
        {
          image:'src/assets/img/buy-comics-digital-comics.png',
          text:'CHARACTERS'
        },
        {
          image:'src/assets/img/buy-comics-merchandise.png',
          text:'COMICS'
        },
        {
          image:'src/assets/img/buy-comics-shop-locator.png',
          text:'MOVIES'
        },
        {
          image:'src/assets/img/buy-comics-subscriptions.png',
          text:'TV'
        },
        {
          image:'src/assets/img/buy-dc-power-visa.svg',
          text:'GAMES'
        }
      ]

    }
  }
}
</script>

<template>
  <h2>- ->Content goes here<- - </h2>
  <nav>
    <li v-for="(comic,index) in comicsList" :key="index">
      <img :src="comic.image" :alt="comic.text">
      <p>{{ comic.text }}</p>

    </li>
  </nav>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;

h2{
  background-color: hsl(0deg 0% 10.98%);
  color: white;
  padding: 2rem 5rem;
}

nav{
  display: flex;
  justify-content: space-evenly;
  list-style-type: none;
  background-color: $color-blue-light;
  color: white;
  padding: 2rem 5rem;

  li{
    display: flex;
    justify-content: space-between;
    margin-left: 1rem;

    img{
      width: 30px;
    }

  }
}

</style>
