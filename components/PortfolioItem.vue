<template>	
	<div class="col-12 col-md-5 mt-4">
		<nuxt-link  
		:to="'/works/'+work.slug"> 
		
          <h4 class="project-client">{{work.client}}</h4>
          <span class="project-category">{{work.category}}</span>        
          <img class="project-thumbnail img-fluid" :src="work.thumbnail">
        
        <p class="project-description">{{work.description}}</p>
        </nuxt-link> 
      	<!-- <nuxt-link :to="'/works/'+slug">	
  			<h4 class="project-client">{{client}}</h4>
  			<span class="project-category">{{category}}</span>  			
  			<img class="project-thumbnail img-fluid" :src="thumbnail">
  		</nuxt-link>
	  		<p class="project-description">{{description}}</p> -->
		</div> 
</template>
<script>

	export default {

		props: {

			work: {
				type: Object
			}
		} // ['category','client','thumbnail','description','slug'],
	};
	// export default {
	// 	components: {
	// 		PortfolioItem
	// 	}
	// }
</script>
<style scoped>

	a {
		text-decoration: none;
	}
	.project-client {
	 
	 	color: #156f9a;
	 	font-size: 1.5em;	
	}
	.project-client::before {

		content: '';
		width: 20px;
		height: 20px;
		display: inline-block;
		margin-right: 20px;
		background-color:  #41fef1;
	}
	.project-category {

		color: grey;
		font-size: 1.1rem;
		margin-left: 40px;
		/*font-weight: bold;*/
	}
	.project-thumbnail {

		margin-bottom: 2rem;
		margin-top: 2rem;
		border-radius: 15px;
		box-sizing: border-box;
    	box-shadow: 6px 5px 12px 1px #b5b5b5
	}
	.project-thumbnail:hover {

		margin-bottom: 2rem;
		margin-top: 2rem;
		border-radius: 15px;
		box-sizing: border-box;
    	box-shadow: 2px 2px 12px 1px #3a89a9;
	}

	.project-description {

		font-size: 1.3rem;
		color: #156f9a;
	}

	

</style>