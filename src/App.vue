<template>
  <div class="menu">
    <a v-for="작명 in 메뉴들" :key="작명">{{작명}}</a>
  </div>
  <div>
    <h4 :style="스타일">
      <ul>
      <li v-for="product in products" :key="product">{{product}}</li>
      <li v-for="(price,i) in price" :key="i" >{{price}}만원</li>
      </ul>
    </h4>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      price: [50,30,60],
      메뉴들: ['HOME','PRODUCTS','ABOUT'],
      products :  ['역삼동원룸', '천호동원룸', '마포구원룸'],
    }
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
 