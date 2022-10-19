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

</style>