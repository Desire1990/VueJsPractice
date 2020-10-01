<template>
    <div class="card">
	    <div class="card-body quote">
	      <slot></slot>
    	</div>
    </div>
 
</template>

<script>
</script>

<style>
    .quote {
        cursor: pointer;
    }
    .quote:hover {
      background-color: red;
      }

   
</style>