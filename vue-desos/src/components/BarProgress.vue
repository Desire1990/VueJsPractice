<template>
	<div class="container">
		<h1>Bar Progress</h1>
		<div class="progress">
		  <div class="progress-bar" :style="{width: (quoteCount/maxQuotes)*100 + '%'}">{{quoteCount}}/{{maxQuotes}}
		  </div>
		</div>
	</div>
</template>
<script>
	export default{
		props:['quoteCount', 'maxQuotes']
}
	
</script>
<style >
	
</style>