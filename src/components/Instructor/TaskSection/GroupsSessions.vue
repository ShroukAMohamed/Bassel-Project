<template>
  <div class="SessionSlider ps-sm-4 pe-sm-4">
    <div
      :id="carouselNo"
      class="carousel slide w-100"
      data-bs-touch="false"
      data-bs-interval="false"
    >
      <div class="carousel-inner Sessions">
        <div class="carousel-item active">
          <div class="d-flex flex-column align-items-center">
            <div class="mt-4">
              <a href="#SessionState" class="me-3 btn btn-outline-primary"
                >Session 1</a
              >
              <a href="#SessionState" class="btn btn-outline-primary"
                >Session 2</a
              >
            </div>
            <div class="mt-4">
              <a href="#SessionState" class="me-3 btn btn-outline-primary"
                >Session 3</a
              >
              <a href="#SessionState" class="btn btn-outline-primary"
                >Session 4</a
              >
            </div>
            <div class="mt-4">
              <a href="#SessionState" class="me-3 btn btn-outline-primary"
                >Session 5</a
              >
              <a href="#SessionState" class="btn btn-outline-primary"
                >Session 6</a
              >
            </div>
          </div>
        </div>
        <div class="carousel-item">
          <div class="d-flex flex-column align-items-center">
            <div class="mt-4">
              <a href="#SessionState" class="me-3 btn btn-outline-primary"
                >Session 7</a
              >
              <a href="#SessionState" class="btn btn-outline-primary"
                >Session 8</a
              >
            </div>
            <div class="mt-4">
              <a href="#SessionState" class="me-3 btn btn-outline-primary"
                >Session 9</a
              >
              <a href="#SessionState" class="btn btn-outline-primary"
                >Session 10</a
              >
            </div>
            <div class="mt-4">
              <a href="#SessionState" class="me-3 btn btn-outline-primary"
                >Session 11</a
              >
              <a href="#SessionState" class="btn btn-outline-primary"
                >Session 12</a
              >
            </div>
          </div>
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        :data-bs-target="carouselNoBtn"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        :data-bs-target="carouselNoBtn"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "GroupsSessions",
  props: ["carouselNo", "carouselNoBtn"],
};
</script>

<style lang="scss" scoped>
div {
  .Hidden {
    display: none;
  }

  .carousel-control-prev,
  .carousel-control-next {
    opacity: 1 !important;
  }
  .carousel-control-next-icon {
    background-image: url("../../../assets/arrows_circle_indicator_right_icon\ \(1\).png");
  }
  .carousel-control-prev-icon {
    background-image: url("../../../assets/arrows_circle_indicator_left_icon.png");
  }
}
</style>
