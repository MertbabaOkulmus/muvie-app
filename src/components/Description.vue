<template>
  <div class="description w-100 d-flex justify-content-center">
    <button class="textDesc descriptionBtn my-5">Get Premium</button>
    <div class="textDesc advantageText">The TMDB Advantage</div>
    <h2 class="millionsText">
      Millions of movies, TV shows and people to discover. Explore now.
    </h2>
    <div class="MovieDatabaseText w-50">
      <h6>
        The Movie Database (TMDB) is a community built movie and TV database.
        Every piece of data has been added by our amazing community dating back
        to 2008. TMDb's strong international focus and breadth of data is
        largely unmatched and something we're incredibly proud of. Put simply,
        we live and breathe community and that's precisely what makes us
        different.
      </h6>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { defineComponent } from "vue";
</script>


<style scoped>
body,
html {
  font-family: Inter;
  font-style: normal;
  text-align: center;
}
.description {
  font-family: Inter;
  font-style: normal;
  text-align: center;
  /* Description */
  position: absolute;
  height: 30%;
  top: 43%;
  background-color: #02b2e3;
}
.descriptionBtn {
  padding: 6px 12px;
  position: absolute;
  width: 137px;
  height: 38px;
  border: none;
  background: #02b2e3;
  border-radius: 3px;

  color: #ffffff;
  flex-grow: 0;
  margin: 0px 10px;
}
.advantageText {
  position: absolute;
  top: 50px;
  color: #b8b8b8;
}
.millionsText {
  position: absolute;
  top: 98px;
  color: #424242;
}
.MovieDatabaseText {
  position: absolute;
  top: 148px;
  color: #545454;
}
</style>