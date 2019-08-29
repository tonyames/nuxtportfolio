<template>
  <header>
    <nav id="topNav" class="navbar navbar-expand-lg">
      <div class="container">
        <nuxt-link to="/" class="">
          <img class="img-fluid" src="~/static/icon.png">Tony Ames
        </nuxt-link>
        <button data-toggle="collapse" data-target="#navbarResponsive" class="navbar-toggler navbar-toggler-right" type="button" aria-controls="navbarResponsive"
                aria-expanded="false" aria-label="Toggle navigation">Menu</button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="nav navbar-nav ml-auto">
            <nuxt-link tag="li" to="/"><a>Work</a></nuxt-link >
            <nuxt-link tag="li" to="/about"><a>About</a></nuxt-link>
            <nuxt-link tag="li" to="/"><a>Hire Me</a></nuxt-link>
          </ul>
        </div>  
      </div>      
    </nav>
  </header>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo,
  }
}
</script>
<style>
  
  /* #MainNav {

    width:50px;
    padding-top: 100px;
    height: 20vh;
    position: fixed;
    bottom: 50px;
    display: flex;
    justify-content: space-around;
    align-items: baseline;
    flex-direction: row;
    box-shadow: 2px 3px 6px rgba(0, 0, 0, 0.16);
    z-index: 1000;
    writing-mode: vertical-lr; 
    font-size: 0.95rem;
    border-top-right-radius:20px;
    background-color: #156f9a;

    } */
  .nav-socials {

    display: flex;
    padding-top: 0;
    /*writing-mode: vertical-lr; */
  }

  li {
      
    list-style: none;
    margin:15px;
  }
  #topNav {

    display: flex;
    justify-content: space-between;
    align-items: center;;
    margin-left: auto;
    font-size: 1.3em;
    color:black;

  }

  .link_hireMe {

    font-size: 1.2rem;
    color: white;
  }
</style>