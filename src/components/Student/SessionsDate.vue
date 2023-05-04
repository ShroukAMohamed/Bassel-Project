<template>
  <div class="d-flex justify-content-between align-items-center">
    <div class="d-flex flex-column">
      <span>{{ Course_Title }}</span>
      <span class="mt-1 mb-1"
        ><i class="fa-solid fa-laptop-code pe-2"></i>{{ Track_Title }}</span
      >
      <span>{{ Session_Date }}</span>
    </div>
    <img
      class="img-fluid"
      src="../../assets/mr-bochelly-IBKyH0V3rew-unsplash@2x.png"
      alt=""
    />
  </div>
</template>

<script>
export default {
  name: "SessionsDate",
  props: ["Course_Title", "Track_Title", "Session_Date"],
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
div {
  span:first-of-type {
    color: #515661;
    font-size: 17px;
    letter-spacing: 0.5px;
    font-weight: 500;
  }
  span:nth-of-type(2) {
    color: #515661;
  }
  span:nth-of-type(3) {
    font-weight: bold;
    font-size: 15px;
  }
  img {
    width: 25%;
    height: 25%;
    @include breakpoints(mobile) {
      width: 35%;
      height: 35%;
    }
  }
}
</style>
