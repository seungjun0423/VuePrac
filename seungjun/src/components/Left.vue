<template>
          <div class="left">
            <div class="title-bar">
                <h2 class="title">지점별 기상/꽃감염 위험도 정보</h2>
                <div class="legend">
                    <div class="card">
                        <ul class="legend-list">
                            <li><span class="circle low"></span><span>낮음</span></li>
                            <li><span class="circle low-some"></span><span>다소낮음</span></li>
                            <li><span class="circle danger"></span><span>위험</span></li>
                            <li><span class="circle danger-very"></span><span>매우위험</span></li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="scroll-hidden">
                <div class="card-list">
                    <div class="list-item">
                        <div class="card">
                            <p class="address">경기도 연천군 미산면 아미리 714</p>
                            <div class="state">
                                <span class="temp">99.9<small>℃</small></span>
                                <span class="circle low"></span>
                            </div>
                            <ul class="weather-list">
                                <li><span class="icon icon-templow"></span><span class="num">99.9</span><small>℃</small></li>
                                <li><span class="icon icon-temphigh"></span><span class="num">99.9</span><small>℃</small></li>
                                <li><span class="icon icon-rainfall"></span><span class="num">99.9</span><small>%</small></li>
                                <li><span class="icon icon-humidity"></span><span class="num">99999</span><small>㎜</small></li>
                            </ul>
                        </div>
                    </div>
                    <div class="list-item">
                        <div class="card">2</div>
                    </div>
                    <div class="list-item">
                        <div class="card">3</div>
                    </div>                    
                </div>
            </div>
        </div>
</template>

<script>
export default {
  name: 'Left-side',
  data(){
    return {
      
    }
  },
  methods:{

  },
  components: {

},
}
</script>

<style>
/* left */

.left {
	display: flex;
	flex-direction: column;
	width: 50%;
	padding: 10px;
}

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
</style>