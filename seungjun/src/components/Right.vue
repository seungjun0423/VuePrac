<template>
  <div class="right">
            <div class="map-box">
                <div class="card">
                    <div class="map-title"><h3>화상병 발생현황</h3></div>
                    <div class="map">
                      <LeaftletMap></LeaftletMap>
                    </div>
                </div>
            </div>
            <div class="map-box">
                <div class="card">
                    <div class="map-title"><h3>꽃 감염 위험도</h3></div>
                    <div class="map"></div>
                </div>
            </div>
            <div class="map-box">
                <div class="card">
                    <div class="map-title"><h3>꽃병징 출현</h3></div>
                    <div class="map"></div>
                </div>
            </div>
            <div class="map-box">
                <div class="card">
                    <div class="map-title"><h3>궤양 활성 출현</h3></div>
                    <div class="map"></div>
                </div>
            </div>
        </div>
</template>

<script>
import LeaftletMap from "./LeafletMap.vue"

export default {
  name:"Right-side",
  data(){
    return;
  },
  components:{
    LeaftletMap,
  }
}
</script>

<style>


/* right */

.right {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-around;
	width: 50%;
	padding: 10px;
}

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