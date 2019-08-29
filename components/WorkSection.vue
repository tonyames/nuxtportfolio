<template>
    <div class="row mt-4 justify-content-around">
        <PortfolioItem v-for="project in projects" 
        :key="project.slug" :work="project"/>

        <!-- <PortfolioItem 
        category = "Website Design"
        client= "Transvie"
        description="Healthcare Insurance for senegalese Diaspora" 
        thumbnail="/projects/thumbnail-three.png"
        slug="transvie"/>

        <PortfolioItem 
        category = "Website and Android App Design "
        client= "Moozicash"
        description="Loyalty Card App" 
        thumbnail="/projects/thumbnail-two.png"
        slug="Moozicash"/>
        <PortfolioItem 
        category = "Website and Android App Design"
        client= "CountryPocket"
        description="Service on Demand platform" 
        thumbnail="/projects/thumbnail-three.png"
        slug="countrypocket"/>    -->
    </div>
</template>
<script>

	import PortfolioItem from '~/components/PortfolioItem';

	export default {

		components : 
		{
			PortfolioItem,
		},
   props: 
    {    
      works: {
        type:Array,
      }
    },

    data () { 
      return {
        projects: [
        {
          category:"Website Design",
          client:"NEPAD IPPF",
          description:"A multi-donor Special Fund hosted by the African Development Bank (AfDB)", 
          thumbnail:"/projects/nepad/thumbnail-one.png",
          slug:"nepad",
        },
        {
          category:"Website Redesign",
          client:"Transvie",
          description:"Healthcare Insurance for senegalese Diaspora", 
          thumbnail:"/projects/transvie/thumbnail-two.png",
          slug:"transvie",
        },
        {
          category:"Website & Android App Design",
          client:"MooziStudio",
          description:"Moozicash th Loyalty Card App", 
          thumbnail:"/projects/moozicash/thumbnail-three.png",
          slug:"moozicash",
        },
        {
          category:"Website and Android App Design",
          client:"CountryPocket",
          description:"Service on Demand platform", 
          thumbnail:"/projects/countrypocket/thumbnail-four.png",
          slug:"countrypocket",
        } 
        ]
      }
    }
	}

</script>
<style>
	
</style>