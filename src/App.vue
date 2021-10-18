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

  <!-- <Fruits /> -->
  <!-- 
  <button @click="add">ADD</button>
  
  <h1>{{reversedMessage}}</h1> -->

  <!-- **워치** -->
<!-- 
  <h1 @click="changeMessage">{{msg}}</h1>
  <h1>{{reversedMessage}}</h1> -->
<!-- 

  클래스와 스타일 바인딩 -->

<!-- 
  <h1 
  v-bind:class="{active: isActive}"
  @click="activate">
    Hello?! ({{isActive}})
  </h1> -->


<!-- 조건부 렌더링 -->
  <!-- <button @click="handler">
    clik me!
  </button>
  <h1 v-if="isShow">
    Hello?
    </h1>
    <h1 v-else-if="count > 3">
      count>3
    </h1>
  <h1 v-else>
    Good~
  </h1> -->

  <!-- 이벤트 핸들링 수식어 -->
  <a href="https://naver.com"
  target="_blank"
  @click.once="handler">
  naver
  </a>


  <!-- 폼 입력 바인딩은 V-model을 사용 -->
  <!-- v-model.lazy  -->
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


  // import Fruits from '~/components/Fruits'
  // export default {
  //   components:{
  //     Fruits
  //   }
  // }

  export default {
    methods:{   // 이벤트 수식어
      handler(){
        console.log('ABC')
      }
    }



    // data(){            //조건부 렌더링
    //   return{
    //     isShow: true,
    //     count:0
    //   }
    // },
    
    
    // data() {
    //   return {
    //     // msg: 'hello?'
    //       isActive: false
    //   }
    // },


    // computed: { //캐싱을 하고나서는 추가 연산이 없음   / 읽기전용임  getter
    //   // reversedMessage(){
    //   //   return this.msg.split('').reverse().join('')
    //   reversedMessage: {
    //     get() {
    //       return this.msg.split('').reverse().join('')
    //     },
    //     set(value) {
    //       this.msg = value
    //     }
    //   }

    // },
    // watch:{
    //   msg(){
    //     console.log('msg', this.msg)
    //   },
    //   reversedMessage(){
    //     console.log('reversedMessage', this.reversedMessage)
    //   }
    // },
    // methods: {
    //   // add() {
    //   //   this.reversedMessage += '!?'
    //   // this.msg +='!?'
    //   // changeMessage(){
    //   //   this.msg='Good!'
    //   activate(){
    //     this.isActive = true
    //   }
    //   }

    // methods:{
    //   handler(){
    //     this.isShow = !this.isShow
    //     this.count += 1
    //   }
    // }

    }
  
  
</script>


<style lang="scss">
  body {
    color: royalblue;
    font-size: 40px;
  }

  .active{
    color: red;
    font-weight: bold;
  }
</style>