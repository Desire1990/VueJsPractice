<template>
    <div class="row">
      <NewQuote v-for= "(quote, index) in quotes" @click.native="DeleteQuote(index)">{{ quote}}</NewQuote>
    </div>
</template>

<script >
	import NewQuote from './NewQuote.vue';
	export default{
		props:['quotes'],

	components:{
		NewQuote
	},
	methods:{
		DeleteQuote(index){
			this.$emit('deleteQuotes', index)
		}
	}
}

	
</script>

<style >
	
</style>