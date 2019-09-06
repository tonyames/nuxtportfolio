<template>
  <header>
    <b-navbar toggleable="lg" type="light" variant="light">
      <div class="container">       
          <nuxt-link class="navbar-brand" to="/">
            <img class="img-fluid" src="~/static/icon.png">Tony Ames
          </nuxt-link>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto align-items-center">
            <nuxt-link tag="li" to="/"><a class="nav-link">Works</a></nuxt-link>
            <nuxt-link tag="li" to="/about"><a class="nav-link">About</a></nuxt-link>
            <b-nav-item href="/resume/resume_Tony_Ames_UX.pdf" target="_blank">Resume</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
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

  :root {
    --mainColor: #41fef1;
  }
  .nav-socials {
    display: flex;
    padding-top: 0;
    /*writing-mode: vertical-lr; */
  }
 

  li {  
    list-style: none;
    margin:15px;
  }
  a {
    color: #000;
    text-decoration: none;
  }
  a:hover {
    text-decoration: none;
    color: #000 !important;
  }

  .nav-link {
    font-size: 1.15rem;   
  }

 .nuxt-link-exact-active a {
  background:
     linear-gradient(
       to bottom, var(--mainColor) 0%,
       var(--mainColor) 100%
     );
    background-position: 0 100%;
    background-repeat: repeat-x;
    background-size: 4px 4px;
  color: #000;
  text-decoration: none;
  transition: background-size .2s;
}


.nav-link {
  position: relative;
}

.nav-link:before {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #000;
  visibility: hidden;
  -webkit-transform: scaleX(0);
  transform: scaleX(0);
  -webkit-transition: all 0.3s ease-in-out 0s;
  transition: all 0.3s ease-in-out 0s;
}

.nav-link:hover:before {
  visibility: visible;
  -webkit-transform: scaleX(1);
  transform: scaleX(1);
}

.nav-link:hover {

  color: #000 !important;
  background:
     linear-gradient(
       to bottom, var(--mainColor) 0%,
       var(--mainColor) 100%
     );
    background-position: 0 100%;
    background-repeat: repeat-x;
    background-size: 4px 50px;
  color: #000;
  text-decoration: none;

}

  .link_hireMe {

    font-size: 1.2rem;
    color: white;
  }
 li a {
  color: #292929;
  }
   .nuxt-link-active a {

    color: #292929;
  }
 
  
</style>