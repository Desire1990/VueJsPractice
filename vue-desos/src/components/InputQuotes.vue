<template>
	<div class="container" >
		<form>
			<div >
				<label><h1>New Quote</h1></label>
				<textarea class="form-control" rows="3" v-model='quote'></textarea>
			</div>
			<div >
				<button type="button" class="btn btn-primary"@click.preventDefault="createNewQuote">New Quote</button><br>
			</div>
		</form>
	</div>	
</template>


<script>
	export default{
		data:function(){
			return{
				quote:''
			}
		},
		methods:{
			createNewQuote(){
				this.$emit('newQuotecreated', this.quote)
				this.quote="" // to stay with empty area
				
			}
		}
	}

</script>

<style>

</style>