<template>
  <main class="page-content">   
    
      <div id=hero>
        <div class="container">
          <div class="row">
            <vue-typed-js :loop="true" :strings="['Hi,I am Tony Ames','a Product Designer helping startups,web agencies and small business build great digital products',
              'With my background as Front End developper i am proficient in taking ideas from concepts to live']">
            <h1 class="typing"></h1>
              
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
      <section class="content-section">
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
      </section>
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

   
  };
</script>

<style>

* {
  box-sizing: border-box;
}

h2 {
  font-size: 2.2rem;
  color: #156f9a;
}
.page-content {
  
  position: relative;
  z-index: 999;
  width: 100%;
  margin-bottom: 20rem;
  background-color: #fff;
}

#hero {

  height: 60vh;
  display: flex;
  align-items: center;
  justify-content: space-around;
  font-weight: 200 !important;
  background-color: #fff;

}

#hero h2 {

  font-size: 3em;

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
