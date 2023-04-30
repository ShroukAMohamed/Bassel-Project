<template>
  <div>
    <div class="d-flex justify-content-between pb-3">
      <span class="fw-bold"
        ><img class="pe-2" src="../../../assets/in-icon.png" alt="" />
        {{ name }}</span
      >
      <div class="pt-2">
        <img src="../../../assets/stars_24.png" alt="" />
        <img src="../../../assets/stars_24.png" alt="" />
        <img src="../../../assets/stars_24.png" alt="" />
        <img src="../../../assets/stars_24.png" alt="" />
        <img src="../../../assets/stars_24.png" alt="" />
      </div>
    </div>
    <div class="line"></div>
    <div
      class="d-flex justify-content-between align-items-center ms-3 pt-1 pb-1"
    >
      <div class="d-flex align-items-center">
        <img
          class="pe-2 web-icon"
          src="../../../assets/MaskGroup2.svg"
          alt=""
        />
        <p class="mb-0">{{ Track }}</p>
      </div>
      <span><i class="fa-solid fa-calendar-days pe-2"></i>{{ date }}</span>
    </div>
    <div class="line"></div>
    <p class="review-text">
      {{ review }}
    </p>
    <div class="line-2"></div>
    <div class="review">
      <div class="d-flex justify-content-end pt-2 pe-3">
        <img class="pe-2" src="../../../assets/person.png" alt="" />
        <div class="d-inline-flex flex-column justify-content-center">
          <span>{{ person }}</span>
          <span class="fw-semibold">{{ job }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjSection",
  props: ["name", "Track", "date", "review", "person", "job"],
};
</script>

<style lang="scss" scoped>
@import "../../global/scss/main.scss";
.web-icon {
  width: 20%;
}
.line {
  border-bottom: 1px solid #acacada6;
  position: relative;
}
.line-2 {
  margin: auto;
  margin-right: 50px;
  width: 30%;
  border-bottom: 1px solid #acacada6;
  position: relative;
}
.review-text {
  width: 75%;
  margin: auto;
  color: #686f7c;
  font-size: 17px;
  letter-spacing: 0.5px;
  padding: 10px 0;
}
.review {
  span {
    font-size: 14px;
  }
}
</style>
