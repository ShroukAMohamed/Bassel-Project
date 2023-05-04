<template>
  <div class="Recommend">
    <div class="d-flex justify-content-between mb-2">
      <p class="text-black">{{ CourseNameR }}</p>
      <div class="star-icon">
        <span> <i class="fa-solid fa-star"></i></span>
        <span> <i class="fa-solid fa-star"></i></span>
        <span> <i class="fa-solid fa-star"></i></span>
        <span> <i class="fa-solid fa-star"></i></span>
      </div>
    </div>
    <div class="line"></div>
    <p class="mt-3">
      {{ DetailsR }}
    </p>
    <div>
      <span
        ><span><i class="fa-solid fa-laptop-code pe-1"></i></span>
        {{ Num_Tracks }}</span
      >
      <span class="ms-4"
        ><span><i class="fa-solid fa-users pe-1"></i></span>
        {{ Num_Groups }}</span
      >
    </div>
    <button class="mb-0 mt-4 btn btn-danger">Enroll Now</button>
  </div>
</template>

<script>
export default {
  name: "ReCommend",
  props: ["CourseNameR", "DetailsR", "Num_Tracks", "Num_Groups"],
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.Recommend {
  position: relative;
  background-color: #dbddf780;
  padding: 20px;
  margin-top: 20px;
  @include breakpoints(mobile) {
    padding: 20px 10px;
  }
  &::after {
    content: "1000 EGP";
    position: absolute;
    right: 0;
    bottom: 6%;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 130px;
    height: 50px;
    padding-left: 20px;
    background-color: #feaa18;
    color: white;
    font-weight: bold;
    clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 25% 100%, 0% 50%);
  }

  .star-icon {
    span {
      color: #ffb12b !important;
      font-size: 17px !important;
      margin: 0 2px;
    }
  }
}
</style>
