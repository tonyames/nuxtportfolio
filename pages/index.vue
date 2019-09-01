<template>
  <main class="page-content">   
    <no-ssr>
          <vue-particles 
          color="#2a2222"
        :particleOpacity="0.5"
        :particlesNumber="60"
        shapeType="circle"
        :particleSize="3"
        linesColor="#000214"
        :linesWidth="2"
        :lineLinked="true"
        :lineOpacity="0.4"
        :linesDistance="150"
        :moveSpeed="6"
        :hoverEffect="true"
        hoverMode="grab"
        :clickEffect="true"
        clickMode="push"/>
    </no-ssr>
      <div id=hero>

        <div class="container">
          <div class="row">
            <vue-typed-js :loop="true" :strings="['Hi,I am Tony Ames','a Product Designer','and Front End developper','i help startups,web agencies and small business build great digital products',
              'i am proficient in taking ideas from concepts to live']">
            <h2 class="typing"></h2> 
            </vue-typed-js>
            <h2></h2><br><br>
            <p class="hero_about typing">.</p>     
          </div>
        </div>
      </div>
      <section class="content-section">
        <div class="container">
          <div class="row mt-2 mb-4">
            <h2>Latest Works</h2>
          </div>
          <WorkSection/>
        </div>
      </section>
      <!-- <section class="content-section">
        <div class="container">
          <div class="row mt-4 mb-4">
            <h2>Work Experience</h2>
          </div>
          <div class="row">
            <div class="col-10">
              <table></table>
            </div>
            <div class="col-12">
              <img class="clients-logo-item" src="/clients/transvie-logo.png">
              <img class="clients-logo-item" src="/clients/kan_logo_red.png">
              <img class="clients-logo-item" src="/clients/Dayo-logo.png">
              <img class="clients-logo-item" src="/clients/logo-moozistudio.png">
              <img class="clients-logo-item" src="/clients/logo-afribills-web.png">
              <img class="clients-logo-item" src="/clients/logo_cpocket.png">
            </div>
          </div>
        </div>
      </section> -->
      <section class="content-section">
        <div class="container">
          <div class="row mt-4 mb-4">
            <h2>Clients</h2>
          </div>
          <div class="row">
            <div class="col-10">
              <p>I've been fortunate to work with some amazing partners. From corporate companies to public organizations, startups and forward-thinking web studios</p>
            </div>
            <div class="col-12">
              <img class="clients-logo-item" src="@/static/clients/Dayo-logo.png">
              <img class="clients-logo-item" src="@/static/clients/kan_logo_red.png">
              <img class="clients-logo-item" src="@/static/clients/logo-afribills-web.png">
              <img class="clients-logo-item" src="@/static/clients/LOGO-MOOZISTUDIO.png">
              <img class="clients-logo-item" src="@/static/clients/transvie-logo.png">
              <img class="clients-logo-item" src="@/static/clients/logo_cpocket.png">
            </div>
          </div>
        </div>
      </section>
  </main>
</template>
<script>

  import Logo from '~/components/Logo.vue'
  import Header from '~/components/Header.vue'
  import PortfolioItem from '~/components/PortfolioItem.vue'
  import WorkSection from '~/components/WorkSection.vue'
  import Footer from '~/components/Footer.vue'



  export default {
    components: {
      Logo,
      Header,
      PortfolioItem,
      WorkSection,
      Footer,
    },
		
    transition: {
      name:'slide-fade'
    },
    
    mounted: function () {
      this.$nextTick(function () {
        // Ce code va être exécuté seulement
        // une fois le rendu de la vue entière terminé
        var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
        (function(){
        var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
            s1.async=true;
            s1.src='https://embed.tawk.to/5d41fb987d27204601c8a58b/default';
            s1.charset='UTF-8';
            s1.setAttribute('crossorigin','*');
            s0.parentNode.insertBefore(s1,s0);
            })();
      })
    }
  }
    


</script>


<style>

* {
  box-sizing: border-box;
}

/* handle transitions  */
/* .page-enter-active, .page-leave-active {
  transition: opacity .7s;
}
.page-enter, .page-leave-active {
  opacity: 0;
} */
 
h2 {
  /* font-size: 2.2rem; */
  color: #3abfd4; /*#1f7782;*/
  font-weight: 600;
} 
.page-content {
  
  position: relative;
  z-index: 999;
  width: 100%;
  margin-bottom: 10rem;
  background-color: #fff;
}

#hero {

  height: 70vh;
  display: flex;
  align-items: center;
  justify-content: space-around;
  font-weight: 200 !important;
  background-color:#3abfd4; /*#00010a;*/
}

.typed-element {

  padding: 15px;
}

#hero h2 {

  font-size: 2em;
  font-weight: 400;
  color: #ffffff;

}

.hero-content-wrapper {
  
  min-height: 40vh;
}

.hero_about {

  font-size: 1.6rem;
}

.clients-logo-item {

  margin:10px;
  width: 125px;
  filter: grayscale(1);

}

.clients-logo-item:hover {

  margin:10px;
  width: 125px;
  filter: grayscale(0);
  transition: ease 

}

.content-section {

  position: relative;
  overflow: hidden;
  padding-top: 5em;
  padding-bottom: 5em;
  background-color: #fff;
}
#particles-js {
  position: absolute;
  width:100%;
}
/*.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
  }*/
</style>
