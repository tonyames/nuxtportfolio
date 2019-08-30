<template>
	<div class="page-content">
		<div class="container">
			<div class="row mt-4 mb-4 align-items-center">
				<div class="col-12 col-md-6 ">
					<h1 class="title">
						{{attributes.client}}
					</h1>
					<h4>{{attributes.description}}</h4>
				</div>
				<div class="col-12 col-md-6 mt-4 mb-4">
					<div>
						<img class="thumbnail" :src="`/projects/${attributes.slug}/_thumbnail.png`">
					</div>	
				</div>
			</div>
			<section class="mt-4 mb-4">
				<div class="row">
					<div class="col-12 col-md-8 ">
						<div class="" v-html="content">
						</div>
					</div>
					<div class="col-12 col-md-4 ">
						<div class="tasks_list_wrapper">
							<h2 style="font-size:2.5em">Task & Roles</h2>
							<ul>
								<li>Information Architecture</li>
								<li>UX/UI Design</li>
								<li>Front End Development</li>	
							</ul>
						</div>
					</div>
				</div>
				<div class="row">
					<div class="col-12 col-md-8 ">
						<div class="">
							<p> ipsum dolor sit amet consectetur adipisicing elit. Quam dicta at unde officia, 
							eos a dolores vel et itaque voluptatibus quae aperiam nobis voluptatem aut voluptate 
							error non voluptates voluptatum </p>
						</div>
					</div>
					<div class="col-12 col-md-4 ">
						
					</div>
				</div>
			</section>
		</div>	
	</div>			
</template>
<script>
	
	export default {

		
		async asyncData ({params}) { 
		
		const res = await import(`~/contents/projects/${params.slug}.md`)
		console.log(res);
		
		// console.log("hii"+ currentSlug);

		// switch (currentSlug) {
		// 	case "nepad":
		// 		content = {

		// 		
		// 	}
		// 		break;

		// 	case "transvie":
		// 		content = {

		// 		client:"Transvie",
		// 		slug:''+ currentSlug +'',
		// 		description:"Healthcare Insurance for senegalese Diaspora",
		// 	}
		// 		break;

		// 	case "moozicash":
		// 		content = {

		// 		client:"MooziStudio",
		// 		slug:''+ currentSlug +'',
		// 		description:"Moozicash the Loyalty Card App",
		// 	}
		// 		break;

		// 	case "countrypocket":
		// 		content = {

		// 		client:"CountryPocket",
		// 		slug:''+ currentSlug +'',
		// 		description:"Get your daily services on demand platform",
		// 	}
		// 		break;
		// 	default:
		// 		break;
		// }
		

      	return {
			  content : res.html,
			  attributes: res.attributes,
			// client:"NEPAD IPPF",
			// slug:"nepad",
			// description:"A multi-donor Special Fund hosted by the African Development Bank (AfDB)", 
			// projects: [
			// {
			// category:"Website Design",
			// client:"NEPAD IPPF",
			// description:"A multi-donor Special Fund hosted by the African Development Bank (AfDB)", 
			// thumbnail:"/projects/thumbnail-one.png",
			// slug:"nepad",
			// },
			// {
			// category:"Website Design",
			// client:"Transvie",
			// description:"Healthcare Insurance for senegalese Diaspora", 
			// thumbnail:"/projects/thumbnail-two.png",
			// slug:"transvie",
			// },
			// {
			// category:"Website & Android App Design",
			// client:"MooziStudio",
			// description:"Moozicash th Loyalty Card App", 
			// thumbnail:"/projects/thumbnail-three.png",
			// slug:"moozicash",
			// },
			// {

			// } 
			// ]
      }
	},
	transition:{
		name:'slide-fade'
	},
	
}
</script>
<style lang="scss">
.page-content {
	overflow: hidden;
}
.thumbnail {
    top: 0px;
    right: 0px;
    width: auto;
    height: 500px;
    object-fit: cover;
    object-position: center center;
    opacity: 1;
    transition: opacity 0.5s ease 0.5s;
}
.tasks_list_wrapper {
	h2 {
		font-size: 2.75rem;
	}
	ul {
		padding:0;
	}
	li {
		font-size: 1.5rem;
		border-bottom: 1px solid rgb(234, 230, 226);;
		padding-bottom: 1.2rem;
	}
}
</style>
