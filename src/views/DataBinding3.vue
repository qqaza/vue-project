<template>
  <label>선택<input type="checkbox" true-value="yes" false-value="no" v-model="checked"></label>
  <p>선택값: {{checked}}</p>

   <!-- v-model => value -->
  <label>text속성: <input type="text" v-bind:value= "ival" > </label>          
  <p>값: {{ival}}</p>

<!--v-bind: attribute의 값을 바인딩. -->
<img v-bind:src="imgSrc" :width="imgWidth">
<input type="text" v-model="textStr">
<!-- input 안에 빈칸이면 비활성화 글이 있으면 활성화 하게 만들기. -->
<button v-bind:disabled="textStr == '' ">Click</button>


</template>

<script>
export default {
   data(){
    return{
      checked: 'yes',
      ival: 'sample',
      imgSrc: 'https://kr.vuejs.org/images/logo.png',
      imgWidth: '100px',
      isTrue: true,
      textStr: ''
    }
  }
}
</script>

