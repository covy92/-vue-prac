<template>
  <!--   
  <h1 @click="increase">
    {{ count }}
    </h1>
  <div v-if="count>4">
    4보다 큽니다!
  </div>
  <ul>
    <Fruit 
    v-for="fruit in fruits" 
    :key="fruit"
    :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul> -->

  <!-- 템플릿 문법 -->
<!-- 
  <h1 v-once @click="add">
    {{msg}}
  </h1>
  <h1 v v-html="msg">  </h1>    v-once는 반응성을 없앰  , v-html 로 html문법을 적용한 상태로 출력  -->
<!-- <h1 :[attr]="'active'"
@[event]="add"
>{{msg}}</h1> v-bind로 속성에 클래스 추가 가능 약어는 : 하나만 사용 -->

<Fruits />

</template>

<script>
  // import Fruit from '~/components/Fruit'
  // export default {
  //   components:{
  //     Fruit
  //   },

  //   data(){
  //     return{
  //       count: 0,
  //       fruits: ['Apple', 'Banana', 'Cherry']
  //     }
  //   },
  //   methods:{
  //     increase(){
  //       this.count +=1
  //     }
  //   }
  // }

  // 템플릿 문법

  // export default {
  //   data() {
  //     return {
  //       // msg: '<div style="color: red;">Hello!!</div>'  // v-html 사용법
  //       msg: 'active',
  //       attr: 'class',
  //       event: 'click'
  //     }
  //   },
  //   methods: {
  //     add() {
  //       this.msg += '!'
  //     }
  //   }
  // }

  //** Computed


  import Fruits from '~/components/Fruits'
  export default {
    components:{
      Fruits
    }
  }

</script>


<style lang="scss">
 .active {
   color: royalblue;
   font-size:100px;
 }
</style>