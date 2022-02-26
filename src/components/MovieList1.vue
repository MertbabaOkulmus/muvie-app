<template>
  <div class="movie">
    <div class="row row-cols-5 d-flex">
      <div v-for="(i, index) in imglist" :key="index">
        <div class="card" style="width: 18rem">
          <img
            :src="'https://image.tmdb.org/t/p/w500' + i.poster_path"
            alt=""
            class="card-img-top"
          />
          <div class="card-body">
            <p class="card-text">
             {{i.title}}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import {
  onMounted,
  onUpdated,
  ref,
  defineProps,
} from "vue";
import axios from "axios";
let imglist = ref();
const props = defineProps<{
  push: any;
}>();

onMounted(async () => {
  await axios
    .get(
      "https://api.themoviedb.org/3/trending/all/day?api_key=e6da8f6ab1d5059c5a68581dd5a973c0"
    )       
    .then(
      (response) => (
        (imglist.value = response.data.results),
        (imglist.value = imglist.value.slice(0, 6))
      )
    );
});
onUpdated(async () => {
  if (props.push === undefined) {
    await axios
      .get(
        "https://api.themoviedb.org/3/trending/all/day?api_key=e6da8f6ab1d5059c5a68581dd5a973c0"
      )
      .then(
        (response) => (
          (imglist.value = response.data.results),
          (imglist.value = imglist.value.slice(0, 6))
        )
      );
  }
  else {
    await axios
    .get(
      "https://api.themoviedb.org/3/search/movie?api_key=e6da8f6ab1d5059c5a68581dd5a973c0&query=" +
        props.push
    )
    .then(
      (response) => (
        (imglist.value = response.data.results),
        (imglist.value = imglist.value.slice(0, 12))
      )
    );
  }
  
});
</script>
<style scoped>
.movie {
  font-family: Inter;
  font-style: normal;
  text-align: center;
  /* Description */
  position: absolute;
  height: auto;
  top: 73%;
}
</style>