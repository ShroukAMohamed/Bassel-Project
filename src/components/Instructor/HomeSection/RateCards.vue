<template>
  <div class="SmallCard mt-4">
    <div class="d-flex justify-content-around align-items-center">
      <div class="d-flex align-items-center">
        <img class="img-fluid me-3" src="../../../assets/cheif1.jpg" alt="" />
        <span>Shon Smith</span>
      </div>
      <div>
        <div class="text-center d-flex flex-column flex-sm-row">
          <span class="me-sm-4">Very Good</span>
          <div class="d-inline">
            <span class="Stars"><i class="fa-solid fa-star me-1"></i></span>
            <span class="Stars"><i class="fa-solid fa-star me-1"></i></span>
            <span class="Stars"><i class="fa-solid fa-star me-1"></i></span>
            <span class="Stars"><i class="fa-solid fa-star me-1"></i></span>
            <span class="Stars"><i class="fa-solid fa-star me-1"></i></span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RateCard",
};
</script>

<style lang="scss" scoped>
.SmallCard {
  background-color: white;
  padding: 8px 0;
  border-radius: 20px;
  img {
    position: relative;
    top: 0;
    left: 0;
    width: 42px;
    object-fit: cover;
    height: 42px;
    border-radius: 50%;
  }
  .Stars {
    color: #ffb12b;
  }
}
</style>
