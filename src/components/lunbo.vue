<template>
<div class="slide-img">
      <a href="xxx">
        <img :src="slides[nowIndex].src" alt="" width="100%">
      </a>
    <h3>{{ slides[nowIndex].title }}</h3>
	<ul class="slide-pages">
      <li @click="goto(prevIndex)"><</li>
      <li v-for="(items,index) in slides" @click="goto(index)">
        <a :class="{on:index == nowIndex}">{{ index+1 }}</a>
      </li>
      <li @click="goto(nextIndex)">></li>
  </ul>
  </div>
</template>

<script>
export default{
  name:'slide-img',
	data () {
      return {
        invTime:2000,
        nowIndex:0,
        slides:[
          {
            src:'../assets/logo.png',
            title:'标题1'
          },
          {
            src:'../assets/logo.png',
            title:'标题2'
          },
          {
            src:'../assets/logo.png',
            title:'标题3'
          }
        ]
      }
    },
    props:{
          slides:{
              type:Array,
              default:[]
          }
      },
    mounted(){
          console.log('slide show.....')
          console.log(this.slides)
 
    },
    methods:{
          goto(index){
              this.nowIndex = index
          }
      }
}
</script>

<style scoped>
  .slide-img{
    width: 500px;
    height: 500px;
    background-color: red;
  }
</style>