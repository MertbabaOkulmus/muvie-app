<template>
    <div class="navBar">
        <div class="Muvimelogo">
            <span>MUVİME</span>
        </div>
        <button class="Buttons btn btn-light">Daha Fazla +</button>
    </div>
</template>






<script lang="ts" setup>
import { defineComponent } from 'vue';

</script>





<style stoped>
.Muvimelogo {
    /* MUVIME */

    position: absolute;
    width: 102px;
    height: 5%;
    left: 72px;
    top: 17px;

    font-family: Inter;
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 29px;
    /* identical to box height */

    color: #000000;
}
.Buttons {
   
    flex-direction: row;
    align-items: flex-start;
  
    position: absolute;
    width: 136px;
    height: 38px;
    left: 620px;
    top: 13px;
    background: rgba(0, 0, 0, 0.1);
  
}
.DarkGhostBtn1 {
}
</style>