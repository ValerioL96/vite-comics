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
          active:false,
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
      ],
      shopList:[
        {
          id:1,
          name:'Shop DC'
        },
        {
          id:2,
          name:'Shop DC Collectibles'
        },

      ],
      dcList:[
      {
          id:1,
          title:'CHARACTERS',
          url:'#',
        },
        {
          id:2,
          title:'COMICS',
          url:'#',
        },
        {
          id:3,
          title:'MOVIES',
          url:'#',
        },
        {
          id:4,
          title:'TV',
          url:'#',
        },
        {
          id:5,
          title:'GAMES',
          url:'#',
        },
        {
          id:6,
          title:'COLLECTIBLES',
          url:'#',
        },
        {
          id:7,
          title:'VIDEOS',
          url:'#',
        },
        {
          id:8,
          title:'FANS',
          url:'#',
        },
        {
          id:9,
          title:'NEW',
          url:'#',
        },
        {
          id:10,
          title:'SHOP',
          url:'#',
        },
        {
          id:11,
          title:'SHOP',
          url:'#',
        }
      ],
      sitesList:[
        {
          id:1,
          site_name:'DC',
          url:'#',
        },
        {
          id:2,
          site_name:'MAD Magazine',
          url:'#',
        },
        {
          id:3,
          site_name:'DC Kids',
          url:'#',
        },
        {
          id:4,
          site_name:'DC Universe',
          url:'#',
        },
        {
          id:5,
          site_name:'DC Power Visa',
          url:'#',
        }
      ], 
      socialsList:[
        {
          id:1,
          image:'src/assets/img/footer-facebook.png',
        },
        {
          id:2,
          image:'src/assets/img/footer-periscope.png',
        },
        {
          id:3,
          image:'src/assets/img/footer-pinterest.png',
        },
        {
          id:4,
          image:'src/assets/img/footer-twitter.png',
        },
        {
          id:5,
          image:'src/assets/img/footer-youtube.png',
        },

      ]

    }
  }
}
</script>

<template>
  <section class="contact-list d-flex">
    <div class="comics">
      <ul>
        <h3>DC COMICS</h3>
        <li v-for="link in navBarList" :key="link.id">
          {{ link.title }}
        </li>
      </ul>
      
      <ul>
        <h3>SHOP</h3>
        <li v-for="shop in shopList" :key="shop.id">
          {{ shop.name }}
        </li>
      </ul>
    </div>
    <ul>
      <h3>DC</h3>
      <li v-for="link in dcList" :key="link.id">
        {{ link.title }}
      </li>

    </ul>
    <ul>
      <h3>SITES</h3>
      <li v-for="site in sitesList" :key="site.id">
        {{ site.site_name }}
      </li>

    </ul>

    <img src="../assets/img/dc-logo-bg.png" alt="logo-footer">
  </section>
  <section class="nav-socials">
    <button> Sign-Up Now</button>
    <nav class="socials">
      <h3>Follow Us</h3>
      <li v-for="social in socialsList" :key="social.id">
        <img :src="social.image" alt="social-image">
      </li>
    </nav>

  </section>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as*;

.contact-list{
  background-image: url(../assets/img/footer-bg.jpg);

  ul{

    list-style-type: none;
    color: white;

    li{
      color: hsl(0deg 0% 47.45%);
    }
  }
}

.nav-socials{
  display: flex;
  justify-content: space-between;
  padding: 2rem 5rem;
  background-color: hsl(0deg 0% 18.82%);

  button{
    background-color: transparent;
    border:solid $color-blue-light;
    color: white;
  }

  nav.socials{
    display: flex;
    list-style-type: none;

    h3{
      font-family: 'Times New Roman', Times, serif;
      font-size: border;
      margin-left: 1rem;
      color: $color-blue-light;
    }

    li{
      margin-left: 1rem;
    }
  }
}
</style>
