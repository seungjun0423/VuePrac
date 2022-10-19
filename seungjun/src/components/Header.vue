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

</style>