<template>
  <div class="d-flex justify-content-between">
    <div class="d-flex flex-column">
      <span>{{ Course_Title }}</span>
      <span class="mt-1 mb-1"
        ><i class="fa-solid fa-laptop-code pe-2"></i>{{ Track_Title }}</span
      >
      <span>{{ Session_Date }}</span>
    </div>
    <img
      class="img-fluid w-25 h-25"
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
}
</style>
