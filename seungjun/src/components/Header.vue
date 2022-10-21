<template>
  <div class="header">
        <div class="logo">
            <img src="../assets/symbol.png" alt="과수화상병 로고"><h1>과수화상병 종합상황판</h1>
        </div>
        <div class="select-area">
            <div class="select-crop">
                <div class="card">
                    <button type="button" class="btn btn-crop active">사과</button>
                    <button type="button" class="btn btn-crop">배</button>
                </div>
            </div>
            <div class="select-date">
                <button type="button" class="btn btn-date">어제</button>
                <button type="button" class="btn btn-date active">오늘</button>
                <button type="button" class="btn btn-date">내일</button>
                <button type="button" class="btn btn-controller">
                    <span class="icon icon-play"></span>
                </button>
            </div>
        </div>
        <div class="current-time">
            <div class="card">
                <span>2022년 10월 13일 (목) 오전 11:00</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name:'fbr-header',
  data(){
    return{

    }
  }
}
</script>

<style>
/* header */

.header {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
	align-items: center;
	padding: 10px 20px;
	padding-top: 20px;
}

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
</style>