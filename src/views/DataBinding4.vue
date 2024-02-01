<template>
  <div class="container" v-bind:class="simpleClass">
    Hello
  </div>

  <!--객체로 만들어서 사용 -->
   <div class="container" v-bind:class="{active: activeValue, 'text-red': redValue }">
    Hello
  </div>

<!--배열로 만들어서 사용 -->
<div class="container" v-bind:class="[activeClass, redClass]">
    Hello
  </div>

  <div style="color: red; background: yellow;">
    style1
  </div>
  <div v-bind:style="{color: att1, background: att2}">
   style2
  </div>
<!--변수로 만들어서 적용 -->
    <div v-bind:style="colorStyle">
   style3
  </div>

  


</template>

<script>
export default {
   data(){
    return{
      simpleClass: 'text-red active',
      activeValue: true,
      redValue: false,  //true 써주면 글자는 빨간색됨.
      activeClass: 'active',
      redClass: 'text-red',
      att1: 'red',
      att2: 'yellow',
      // colorStyle: 'color: red; background: yellow'
      colorStyle:{
        color: 'red',
        background: 'yellow'
      }
    }
  },
  
  mounted(){
    console.log(this)
  },
  methods: {// 이벤트 실행함수...}
  }
}

</script>

<style>
  .container{
    width: 100%;
    height: 50px;
  }
  .active{
    background-color: yellow;
    font-weight: bold;
  }
  .text-red{
    color: red;
  }
</style>

