<template>
  <div class="hero w-100">
    <div class="w-80">
      <input
        v-model="search"
        type="text"
        class="search w-75 form-contro"
        placeholder="Search for a movie, person or genre"
        aria-label="Recipient's username"
        aria-describedby="button-addon2"
      />
      
     
      <button
        class="SearchBtn btn btn-danger"
        @click="handleClik"
        type="button"
        id="button-addon2"
      >
        Search
      </button>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { onMounted, onUpdated, defineEmits, ref } from "vue";
let description = ref();
let search = ref();
const emit = defineEmits(['actionCaptured'])
const handleClik =()=>{
    emit('actionCaptured',search.value);
}

</script>


<style scoped>
body,
html {
  font-family: Inter;
  font-style: normal;
}
.hero {
  /* background */
  position: absolute;
  height: 37%;
  top: 64px;
  background: url("../assets/images/background.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
.search {
  /* Search */
  position: absolute;

  height: 64px;
  left: 10%;
  top: 219px;
  background: rgba(255, 255, 255, 0.95);
  border-radius: 3px;
}
.SearchBtn {
  position: absolute;
  width: 85px;
  height: 38px;
  top: 234px;
  right: 16%;
  background: #e22a2a;
  border-radius: 3px;
}
</style>