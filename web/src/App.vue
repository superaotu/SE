<template>
	<div class="column flex1">
		
		<!-- <img alt="Vue logo" src="./assets/logo.png"> -->
		<SearchInput msg="Welcome to Your Vue.js App" />
		<ResultList></ResultList>
		<!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
	</div> 
</template>

<script>

import SearchInput from "./components/SearchInput.vue"

import ResultList from "./components/ResultList.vue"
export default {
  name: 'App',
  components: {
    SearchInput,ResultList
  } 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  
}
div{
	display: flex;
}
.flex1{
	flex: 1;
}
.column{
	flex-direction: column;
}
</style>
