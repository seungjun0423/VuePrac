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
body{
  margin:0px;
}

#app
{
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

*, *:before, *:after
{
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}

h1, h2, h3, h4, h5, h6
{
	font-weight: 700;
}

a, button
{
	cursor: pointer;
}

ul, ol
{
	list-style: none;
	padding: 0;
	margin: 0;
}

.card
{
	position: relative;
	width: 100%;
	border-radius: 15px;
	box-shadow: 0 5px 5px rgba(28,70,148,.1);
}

.btn
{
	font-size: 1em;
	padding: 10px 20px;
	border: transparent;
	border-radius: 7px;
	background-color: #ffffff;
	box-shadow: 0 5px 5px rgba(28,70,148,.1);
}

.icon
{
	display: inline-block;
	height: 16px;
	padding: 0;
	margin: 0;
	background-repeat: no-repeat;
	background-position: center top;
}

.icon-play
{
	width: 15px;
	background-image: url('./assets/icon-play.png');
}

.icon-stop
{
	width: 15px;
	background-image: url('./assets/icon-stop.png');
}

.icon-templow
{
	width: 14px;
	background-image: url('./assets/icon-templow.png');
}

.icon-temphigh
{
	width: 14px;
	background-image: url('./assets/icon-temphigh.png');
}

.icon-rainfall
{
	width: 14px;
	background-image: url('./assets/icon-rainfall.png');
}

.icon-humidity
{
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
.header {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
	align-items: center;
	padding: 10px 20px;
	padding-top: 20px;
}
.main {
	display: flex;
	justify-content: space-around;
	width: 100%;
	height: 100%;
}
.left {
	display: flex;
	flex-direction: column;
	width: 50%;
	padding: 10px;
}
.right {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-around;
	width: 50%;
	padding: 10px;
}
.map-box {
	position: relative;
	width: 50%;
	padding: 10px;
}

/* header */
.logo img, .logo h1, .select-crop, .select-date {
	display: inline-block;
	vertical-align: top;
}
.logo h1 {
	font-size: 1.750em;
	font-family: 'nanumsquare', sans-serif;
	padding: 5px 0 0 0;
	margin: 0 0 0 10px;
}
.select-crop {
	margin: 0 20px;
}
.select-crop .card {
	padding: 5px;
	border-radius: 12px;
	background-color: #ffffff;
}
.btn.btn-crop {
	color: #666666;
	font-size: 1.125em;
	font-weight: 700;
	padding: 10px 30px;
	box-shadow: none;
}
.btn.btn-crop:hover, .btn.btn-crop:focus {
	color: #368bdc;
}
.btn.btn-crop.active {
	color: #ffffff;
	border-radius: 10px;
	background-color: #368bdc;
}
.btn.btn-date {
	color: #ffffff;
	font-size: 1.125em;
	font-weight: 700;
	padding: 15px 35px;
	margin: 0 5px;
	border-radius: 12px;
	background-color: rgba(54,139,220,.3);
}
.btn.btn-date:hover, .btn.btn-date:focus {
	background-color: rgba(54,139,220,.6);
}
.btn.btn-date.active {
	background-color: rgba(54,139,220,1);
}
.btn.btn-controller {
	padding: 6px 10px;
	margin: 0 5px;
	border-radius: 10px;
}
.btn.btn-controller:hover, .btn.btn-controller:focus {
	background-color: #eeeeee;
}
.current-time .card {
	color: #ffffff;
	font-weight: 700;
	padding: 10px 15px;
	background-color: rgba(54,139,220,.5);
}

/* left */
.title-bar {
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 10px;
}
.title-bar .title {
	font-size: 1.375em;
	font-family: 'nanumsquare', sans-serif;
	padding: 0;
	margin: 0;
}
.legend .card {
	padding: 10px 10px;
	background-color: #ffffff;
}
.legend-list li {
	display: inline-block;
	margin: 0 5px;
}
.circle {
	display: inline-block;
	width: 16px;
	height: 16px;
	vertical-align: top;
	margin-top: 2px;
	margin-right: 5px;
	border-radius: 8px;
	background-color: #eeeeee;
}
.circle.low {
	background-color: #30731f;
}
.circle.low-some {
	background-color: #ffff4a;
}
.circle.danger {
	background-color: #f09f34;
}
.circle.danger-very {
	background-color: #e72d20;
}
.scroll-hidden {
	position: relative;
	width: 100%;
	height: 100%;
	overflow: hidden;
}
.card-list {
	display: flex;
	flex-wrap: wrap;
	/* height: 800px;
	margin-right: -17px; */

	position: absolute;
	top: 0;
	right: -17px;
	left: 0;
	bottom: 10px;

	overflow-y: scroll;
}
.card-list .list-item {
	width: 25%;
	padding: 10px;
}
.card-list .list-item .card {
	width: 100%;
	min-height: 150px;
	vertical-align: top;
	padding: 15px;
	background-color: #ffffff;
}
.card-list .address {
	font-size: 0.875em;
	font-weight: 700;
	padding: 0;
	margin: 0 0 15px 0;
}
.card-list .state {
	width: 100%;
	height: 30px;
}
.card-list .state .temp {
	float: left;
	font-size: 1.250em;
	font-weight: 700;
}
.card-list .state .circle {
	float: right;
	margin-top: 5px;
}
.weather-list li {
	display: inline-block;
	width: 45%;
	font-size: 0.875em;
	vertical-align: top;
	margin-top: 5px;
}
.weather-list li .icon {
	margin-right: 5px;
}
.weather-list li span {
	vertical-align: top;
}

/* right */
.map-box .card {
	height: 100%;
	overflow: hidden;
}
.map-box .map-title {
	position: absolute;
	top: 10px; left: 10px;
	padding: 10px;
	background-color: #ffffff;
	border-radius: 10px;
	z-index: 10;
}
.map-box .map-title h3 {
	font-size: 1.125em;
	font-family: 'nanumsquare', sans-serif;
	line-height: 1em;
	padding: 0;
	margin: 0;
}
.map-box .map {
	position: relative;
	width: 100%;
	height: 100%;
	background-color: #a6c8e9;
	z-index: 1;
}

</style>
