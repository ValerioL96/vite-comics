<script>
export default{
  data() {
    return{
      navBarList:[
        {
          id:1,
          title:'CHARACTERS',
          active:false,
          url:'#',
        },
        {
          id:2,
          title:'COMICS',
          active:true,
          url:'#',
        },
        {
          id:3,
          title:'MOVIES',
          active:false,
          url:'#',
        },
        {
          id:4,
          title:'TV',
          active:false,
          url:'#',
        },
        {
          id:5,
          title:'GAMES',
          active:false,
          url:'#',
        },
        {
          id:6,
          title:'COLLECTIBLES',
          active:false,
          url:'#',
        },
        {
          id:7,
          title:'VIDEOS',
          active:false,
          url:'#',
        },
        {
          id:8,
          title:'FANS',
          active:false,
          url:'#',
        },
        {
          id:9,
          title:'NEWS',
          active:false,
          url:'#',
        },
        {
          id:10,
          title:'SHOP',
          active:false,
          url:'#',
        },
      ]
    }
  }
}

</script>

<template>
  <header>

    <div class="header bg-white px-5 py-2 mt-3 ">
    <img src="../assets/img/dc-logo.png" alt="logoDC">
  <nav class="navbar">
   <li v-for="link in navBarList" :key="link.id" :class="(link.active)? 'active' : '' ">
    {{ link.title }}
   </li>
  </nav>
  </div>
 

  </header>
 
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as*;

div.header{
  display: flex;
  justify-content: space-between;
  align-items: center;
 
  

  nav{
  display: flex;
  list-style-type: none;

  li{
    margin-left: 1rem;
    &.active{
      color: $color-blue-light;
      border-bottom:  solid $color-blue-light;
    }
  }
}

}


</style>
