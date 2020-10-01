<template>
<div id="app">
		<div class="container">
			<div class="container text-center">
				<BarProgress :quoteCount='quotes.length' :maxQuotes= "maxQuotes"></BarProgress>
			</div>

			<div class="container text-center">
				<InputQuotes @newQuotecreated='newQuote'></InputQuotes>
			</div><br>

			<div class="card">
				<h1 class="text-center">All Quotes here</h1><hr>
			    <div class="card-body ">
			      <Quotes :quotes="quotes" @deleteQuotes= "deleteQuote"></Quotes>
			    </div>
			</div>
						
			</div><br>
			<div class="container">
				<div class="alert alert-info text-center"> 
					<strong>Info : One  click on quote to delete it!</strong>
				</div>
			</div>
		</div>
	</div>


</template>



<script>
	import BarProgress from './components/BarProgress.vue';
	import Quotes from  './components/Quotes.vue';
	import InputQuotes from  './components/InputQuotes.vue';
	export default{
  		data:function(){
  			return{
  				quotes:['The default quote one'],
  				maxQuotes:10 
  			}
  		},
  		methods:{
  			newQuote(quote ){
  				if (this.quotes.length >= this.maxQuotes){
					return alert('Delete some quotes to continue adding again!!!');
				}
  				this.quotes.push(quote);
  				// if( this.quote = " "){
  				// 	this.quotes.pop(quote);  					
  				// }
  			},
  			deleteQuote(index){
  				this.quotes.splice(index, 1);
  			}
  		},

	  	components:{
	  		Quotes,
	  		InputQuotes,
	  		BarProgress

	  	}
 
  }

</script>
<style>

</style>

