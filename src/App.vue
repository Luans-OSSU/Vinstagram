<template>
  <div id="app">
    <div class="app-phone">
      <div class="phone-header">
        <span class="title">Vinstagram</span>
      </div>
      <phone-body
        :step="step"
        :posts="posts"
        :filters="filters"
        :image="image"
        :selectedFilter="selectedFilter"
        v-model="caption"
      />
      <div class="phone-footer">
        <div class="home-cta">
          <i class="fas fa-home fa-lg"></i>
        </div>
        <div class="upload-cta">
          <i class="fas fa-plus-square fa-lg"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PhoneBody from "./components/PhoneBody";

import posts from "./data/posts.js";
import filters from "./data/filter.js";

export default {
  name: "app",
  data() {
    return {
      step: 1,
      posts,
      filters,
      image: "",
      selectedFilter: "",
      caption: ""
    }
  },
  components: {
    "phone-body": PhoneBody
  }
};
</script>

<style lang="scss" src="./styles/app.scss">
</style>
