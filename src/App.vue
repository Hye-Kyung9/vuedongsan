<template>
  <div class="menu">
    <a v-for="작명 in 메뉴들" :key="작명">{{작명}}</a>
  </div>
  <div>
    <!-- <div v-for="(a,i) in products" :key="i">
      <h4>{{products[i]}}</h4>
      <p>50만원</p>
    </div> -->
    <div>
      <h4>{{products[0]}}</h4>
      <p>50만원</p>
      <button @click="신고수[0]++">허위매물신고</button>
      <span>신고수 : {{신고수[0]}}</span>
    </div>
    <div>
      <h4>{{products[1]}}</h4>
      <p>60만원</p>
      <button @click="신고수[1]++">허위매물신고</button>
      <span>신고수 : {{신고수[1]}}</span>
    </div>
    <div>
      <h4>{{products[2]}}</h4>
      <p>70만원</p>
      <button @click="신고수[2]++">허위매물신고</button>
      <span>신고수 : {{신고수[2]}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      신고수 : [0,0,0],
      메뉴들: ['HOME','PRODUCTS','ABOUT'],
      products :  ['역삼동원룸', '천호동원룸', '마포구원룸'],
    }
  },
  methods:{
    // increase(){
    //   this.신고수 ++;
    // }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.menu {
  background : darkslateblue;
  padding : 15px;
  border-radius : 5px;
}
.menu a {
  color : white;
  padding : 10px;
}
li, ol, ul {
  list-style: none;
}
</style>
 