<template>
	<div class="box">
		<input type="text" placeholder="请输入搜索内容" :value="count">
		<button>搜索</button>
	</div>
</template>
<script>
	export default {
	  name: 'SearchInput',
	  props: {
	    msg: String
	  },
	  setup(){
	    let count = 0
	    const change = () => count++
	    return { count, change }
	  }
	}
</script>

<style scoped>
	input{
		width: 17rem;
		font-size: 1.25rem;
		outline: none;
		border: 2px solid #5C6370;
	}
	input:focus{
		border: 2px solid #0080FF;
	}
	button{
		background-color: rgb(70,98,217);
		outline: none;
		border: none;
		border-radius: 0 !important;
		width: 6rem;
		height: 3rem;
		letter-spacing: 0.25rem;
		color: white;
		font-size: 1.2rem;
	}
	button:hover{
		background-color: rgba(70,98,217,.9);
	}
	.box{
		padding: 0.5rem 1.25rem;
		border-bottom: 1px solid gray;
	}
	
</style>
