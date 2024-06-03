<template>
  <div class="black-bg" v-if="isModalOpen == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="isModalOpen = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="(menu,i) in 메뉴들" :key="i">{{menu}}</a>
  </div>
  <div>
    <div v-for="room in rooms" :key="room.id">
      <img :src="room.image" class="room-img">
      <h4>{{ room.title }}</h4>
      <p>
        {{ room.content }} <br/>
        {{ room.price }}원
      </p>
    </div>
  </div>

</template>

<script>
import data from'./assets/oneroom';

export default {
  name: 'App',
  data(){
    return {
      rooms : data,
      isModalOpen : false,
      reportCount : [0,0,0],
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
body {
  margin : 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height:100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}
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
.room-img{
  width : 100%;
  margin-top: 40px;
}
</style>
 