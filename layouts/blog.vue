<template>
	<div>
		<Header></Header>
		<div class="container ">
			<div class="row">
				<div class="col-12 col-md-2 ">
					<h1 class="title">
						{{title}}
					</h1>
				</div>
				<div class="col-12 col-md-10 ">
					<div>
						<img class="img-fluid" :src="'/projects/'+ slug +'/'+ slug+'.png'"
						>
					</div>
				</div>
			</div>
			<div class="row">
				<div class="col-12 col-md-4 ">
					<div class="content">
						
					</div>
				</div>
				<div class="col-12 col-md-8 ">
					
				</div>
			</div>
			
			
		</div>		
	</div>
</template>
<script>
	import Header from '~/components/Header.vue'

	export default {
		props: {
			title :{
				type:String
			},
			slug : {
				type: String
			}
		},
		components: {

		Header,

		},

		
	}


	
</script>
<style>
	
</style>