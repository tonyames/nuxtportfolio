<template>
    <div class="row mt-4 justify-content-around">
        <PortfolioItem v-for="project in projects" 
        :key="project.slug" :work="project"/>
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
          category:"Android App Design",
          client:"E-Training Platform",
          description:"How a Company train their staff on a digital era", 
          thumbnail:"/projects/e-training-platform/thumbnail-five.png",
          slug:"e-training-platform",
        },
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
          description:"Moozicash the digital loyalty App", 
          thumbnail:"/projects/moozicash/thumbnail-three.png",
          slug:"moozicash",
        },
        {
          category:"Website and Android App Design",
          client:"CountryPocket",
          description:"Daily services on demand platform", 
          thumbnail:"/projects/countrypocket/thumbnail-four.png",
          slug:"countrypocket",
        } 
        ]
      }
    }
	}

</script>
<style>
	* {
  box-sizing: border-box;
}
</style>