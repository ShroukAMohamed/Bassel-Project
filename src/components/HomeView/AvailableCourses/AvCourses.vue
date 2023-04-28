<template>
  <div class="Card m-auto">
    <img
      class="img-fluid"
      src="../../../assets/mr-bochelly-IBKyH0V3rew-unsplash.png"
      alt=""
    />
    <p class="d-flex justify-content-between mt-3">
      Web Development
      <span
        ><i class="fa-solid fa-star me-1"></i>
        <i class="fa-solid fa-star me-1"></i>
        <i class="fa-solid fa-star me-1"></i>
        <i class="fa-solid fa-star me-1"></i
      ></span>
    </p>
    <p>
      Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi
      in nibh faucibus, iaculis lorem vitae, cursus velit
    </p>
    <router-link to="/CourseContent" class="btn btn-outline-secondary"
      >See More</router-link
    >
  </div>
</template>

<script>
export default {
  name: "AvCourses",
};
</script>

<style lang="scss" scoped>
.Card {
  background-color: #f2f2f2;
  padding: 20px;
  width: 100%;
  max-width: 450px;
  p {
    font-size: 16px;
  }
  p:first-of-type {
    font-weight: bold;
    span {
      color: #ffb12b;
      font-size: 15px;
    }
  }
  p:last-of-type {
    color: #515661;
    font-size: 14px;
    width: 88%;
    letter-spacing: 1px;
  }
  a {
    font-size: 14px;
  }
}
</style>
