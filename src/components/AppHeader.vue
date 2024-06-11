<script>
export default{
  data() {
    return{
      navList:[
        {
          message:'CHARACTERS'
        },
        {
          message:'COMICS'
        },
        {
          message:'MOVIES'
        },
        {
          message:'TV'
        },
        {
          message:'GAMES'
        },
        {
          message:'COLLECTIBLES'
        },
        {
          message:'VIDEOS'
        },
        {
          message:'FANS'
        },
        {
          message:'NEWS'
        },
        {
          message:'SHOP'
        },
      ]

    }
  }
}

</script>

<template>
  <div class="header">
    <img src="../assets/img/dc-logo.png" alt="logoDC">
  <nav class="navbar">
    <li v-for="(element, index) in navList" :key ="index">
      {{ element.message }}
    </li>
  </nav>
  </div>
 
</template>

<style scoped>

div.header{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 5rem;

  nav{
  display: flex;
  list-style-type: none;

  li{
    margin-left: 1rem;
  }
}

}


</style>
