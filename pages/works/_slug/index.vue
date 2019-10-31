<template>
	<div class="page-content">
		<div class="container">
			<div class="row mt-4 mb-4 align-items-center">
				<div class="col-12 col-md-6 ">
					<div class="title">
						<h1>{{attributes.project}}</h1>
						<h3>{{attributes.description}}</h3>
					</div>
				</div>
				
				<div class="col-12 col-md-6 mt-4 mb-4">
					<div>
						<img class="thumbnail" :src="`/projects/${attributes.slug}/_thumbnail.png`">
					</div>	
				</div>
			</div>
			<section class="mt-4 mb-4">
				<div class="row">
					<div class="col-12 col-md-9 ">
						<div class="" v-html="content">
						</div>
					</div>
					<div class="col-12 col-md-3 ">
						<div class="">
							<div class="tasks_list_wrapper">
								<h3>Client</h3>
								<ul>
									<li>{{attributes.client}}</li>
									<li> <a class="client-site-link":href="`${attributes.website}`" target="_blanl">{{attributes.website}}</a></li>	
								</ul>
							</div>
						</div>
						<div class="">
							<div class="tasks_list_wrapper">
								<h3>Task & Roles</h3>
								<ul>
									<li>Information Architecture</li>
									<li>UX/UI Design</li>
									<li>Front End Development</li>	
								</ul>
							</div>
						</div>
					</div>
				</div>
				<div class="row">
					<div class="col-12 col-md-8 ">
						
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
		
		const res = await import(`~/contents/en/projects/${params.slug}.md`)
		console.log(res);

      	return {
			  content : res.html,
			  attributes: res.attributes,
      }
	},
	transition:{
		name:'slide-fade'
	},
	
}
</script>
<style lang="scss">
* {
  box-sizing: border-box;
}

.page-content {
	overflow: hidden;
}

.title {
	h1 {
		font-size: 3.5rem;
		color: #007e92;
	}
	h3 {
		margin-top: 0;
    	margin-bottom: 0;
	}
}

h2,h3,h4 {
	margin-top:2rem;
	margin-bottom: 2rem;
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

.client-site-link, .client-site-link:hover {

	color:  #007e92;
}
.tasks_list_wrapper {
	h2 {
		font-size: 2.75rem;
	}
	ul {
		padding:0;
	}
	li {
		font-size: 1.3rem;
		border-bottom: 1px solid rgb(234, 230, 226);;
		padding-bottom: 1.2rem;
	}
}
</style>
