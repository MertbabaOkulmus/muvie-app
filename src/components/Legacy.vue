<template>
    <div class="legacy w-100 d-flex flex-row">
        <div class="muvi d-flex flex-row ">
            <div  style="font-size:24px">
            <span>MUVİME</span>
        </div>
        <div class="reserved mx-5" style="font-size:18px">
            <span>© 2021 Tübitak. All rights reserved.</span>
        </div>
        </div>
        
        <div class="terms">
            <span class="mx-3">Terms of Use</span>
            <span class="mx-3">API Terms of Use</span>
            <span class="">Privacy Policy</span>
        </div>
    </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    name: "App"
});
</script>
<style scoped>
body,
html {
    font-family: Inter;
    font-style: normal;
}
.legacy {
    position: absolute;
    height: 29px;
    top: 1652px;
    font-weight: 800;
    left: 0%;
    right:0%;
}
.muvi{
    position: absolute;
    left: 5%;
}
.terms{

     position: absolute;
    right:5%;
}
</style>