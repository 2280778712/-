/*eslint eol-last: ["error", "always"]*/
<template>
	<div class="container">
		<div class="test">啦啦啦</div>
		<div class="test">撒旦撒</div>
		<div class="test spe">撒大苏打</div>
		<div class="test">风格的</div>
		<div class="test">广汇股份</div>
	</div>
</template>

<script>
export default{
  name: 'container',
  data () {
    return {

    }
  }
}
</script>

<style scoped>
.container{
width: 100%;
height: 7rem;
/*background-color: white;*/
font-size: 16px;
bottom: 0;
position: absolute;
display: flex;
flex-wrap: nowrap;
flex-direction: row;
justify-content:space-around;
/*border:1px solid #000;*/
}
.test{
margin-top: 1.95rem;
color: white;
width: 3.2rem;
height: 3.2rem;
background-color: brown;
float: left;
border-radius: 5px;
box-shadow: -0.4em 0.3em 0.6rem black;
}
.spe{
background-color: blue;
width: 4rem;
height: 4rem;
margin-top: 1.5rem;
}
</style>