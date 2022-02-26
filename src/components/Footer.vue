<template>
  <div class="row footer w-100">
    <div class="col-3 mt-5">
      <h5 class="HeaderFooter TheBasicsHeader mb-4">{{ thebasicsheader }}</h5>
      <div class="TextFooter TheBasicsText">
        <div :key="index" v-for="(val, index) in list3">
          {{ val }}
        </div>
      </div>
    </div>
    <div class="col-3 mt-5">
      <h5 class="HeaderFooter GetInvolvedHeader mb-4">{{ getinvolvedheader }}</h5>
      <div class="TextFooter GetInvolvedText">
        <div :key="index" v-for="(val, index) in list2">
          {{ val }}
        </div>
      </div>
    </div>

    <div class="col-3 mt-5">
      <h5 class="HeaderFooter CommunityHeader mb-4">{{ communityheader }}</h5>
      <div class="TextFooter CommunityText">
        <div :key="index" v-for="(val, index) in list1">
          {{ val }}
        </div>
      </div>
    </div>
    <div class="col-2 mx-auto mt-5">
      <h5 class="mb-4">{{ socialheader }}</h5>
      <div class="TextFooter social d-flex flex-row">
        <div class="icon facebook mx-2">
          <img alt="facebook" src="../assets/icons/facebook.png" />
        </div>
        <div class="icon instagram mx-2">
          <img alt="instagram" src="../assets/icons/instagram.png" />
        </div>
        <div class="icon twitter mx-2">
          <img alt="twitter" src="../assets/icons/twitter.png" />
        </div>
        <div class="icon youtube ">
          <img alt="youtube" src="../assets/icons/youtube.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { defineProps, ref } from "vue";
const communityheader = ref("COMMUNITY");
const props = defineProps<{
  list1: string[];
  list2: string[];
  list3: string[];
}>();

const getinvolvedheader = ref("GET INVOLVED");
const thebasicsheader = ref("THE BASICS");
const socialheader = ref("SOCIAL");
</script>

<style scoped>
html,
body {
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 150%;
}
.footer {
  /* Footer */
  position: absolute;
  height: 23%;
  left: 0px;
  top: 133%;
  /* background */
  background: #032541;
  text-align: right;
  color: #ffffff;
}
.social{
    position: absolute;
    right: 5%;
}
</style>