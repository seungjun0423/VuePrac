<template>
  <div class="Wrapper">
    <l-map style="height: 40vh" >
      <l-tile-layer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"></l-tile-layer>
    </l-map>
  </div>
</template>


<script>
import "leaflet/dist/leaflet.css"
import { LMap, LTileLayer,} from "@vue-leaflet/vue-leaflet";
import KOREA from "../data/KOREA-MAP-V3.json"



export default {
  name:"LeaftletMap",
  
  data(){
    return {
      MAP:KOREA,
    };
  },

  components: {
    LMap,
    LTileLayer,
  },

}
</script>


<style>
.Wrapper {
  display: flex;
  width:100vw;
  overflow: hidden;
  justify-self: center;
  align-content: center;
}

</style>