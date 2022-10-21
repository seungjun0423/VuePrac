<template>
  <div class="wrap">
    <Header></Header>
    <div class="main">
      <Left></Left>
      <Right></Right>
    </div>
</div>
</template>


<script>
import Header from "./components/Header.vue";
import Left from "./components/Left.vue";
import Right from "./components/Right.vue";

export default {
  name: 'app',
  data(){
    return {
    }
  },
  methods:{

  },
  components: {
    Header,
    Left,
    Right
},
}
</script>


<style>
body {
  margin:0px;
}

#app {
	font-family: 'Nanum Gothic', '돋움', sans-serif;
	font-size: 16px;
	height: 100vh;
  width: 100vw;
	font-weight: 400;
	margin: 0px;
	padding: 0px;
	color: #222222;
	background-color: #ffffff;
}

*, *:before, *:after {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}

h1, h2, h3, h4, h5, h6 {
	font-weight: 700;
}

a, button {
	cursor: pointer;
}

ul, ol {
	list-style: none;
	padding: 0;
	margin: 0;
}

.card {
	position: relative;
	width: 100%;
	border-radius: 15px;
	box-shadow: 0 5px 5px rgba(28,70,148,.1);
}

.btn {
	font-size: 1em;
	padding: 10px 20px;
	border: transparent;
	border-radius: 7px;
	background-color: #ffffff;
	box-shadow: 0 5px 5px rgba(28,70,148,.1);
}

.icon {
	display: inline-block;
	height: 16px;
	padding: 0;
	margin: 0;
	background-repeat: no-repeat;
	background-position: center top;
}

.icon-play {
	width: 15px;
	background-image: url('./assets/icon-play.png');
}

.icon-stop {
	width: 15px;
	background-image: url('./assets/icon-stop.png');
}

.icon-templow {
	width: 14px;
	background-image: url('./assets/icon-templow.png');
}

.icon-temphigh {
	width: 14px;
	background-image: url('./assets/icon-temphigh.png');
}

.icon-rainfall {
	width: 14px;
	background-image: url('./assets/icon-rainfall.png');
}

.icon-humidity {
	width: 14px;
	background-image: url('./assets/icon-humidity.png');
}

/* layout */
.wrap {
	display: flex;
    flex-direction: column;
	width: 100%;
	height: 100%;
	padding: 0;
	margin: 0;
	background-color: #d6e2ee;
}

.main {
	display: flex;
	justify-content: space-around;
	width: 100%;
	height: 100%;
}

.map-box {
	position: relative;
	width: 50%;
	padding: 10px;
}

</style>
