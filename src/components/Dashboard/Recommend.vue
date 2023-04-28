<template>
  <div class="Recommend">
    <div class="d-flex justify-content-between mb-2">
      <p class="text-black">Course Title here</p>
      <div class="star-icon">
        <span> <i class="fa-solid fa-star"></i></span>
        <span> <i class="fa-solid fa-star"></i></span>
        <span> <i class="fa-solid fa-star"></i></span>
        <span> <i class="fa-solid fa-star"></i></span>
      </div>
    </div>
    <div class="line"></div>
    <p class="mt-3">
      Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi
      in nibh faucibus,
    </p>
    <div>
      <span
        ><span><i class="fa-solid fa-laptop-code pe-1"></i></span> 4
        Tracks</span
      >
      <span class="ms-4"
        ><span><i class="fa-solid fa-users pe-1"></i></span> 2 Groups</span
      >
    </div>
    <button class="mb-0 mt-4 btn btn-danger">Enroll Now</button>
  </div>
</template>

<script>
export default {
  name: "ReCommend",
};
</script>

<style lang="scss" scoped>
.Recommend {
  position: relative;
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
