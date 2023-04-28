<template>
  <div class="Card">
    <div class="d-flex justify-content-around align-items-center pt-2 pb-2">
      <div class="challenge">
        <span class="d-block">Challenge 01</span>
        <span>XX of total XX</span>
      </div>

      <div class="skill mt-2">
        <div class="outer">
          <div class="inner">
            <div id="number"></div>
          </div>
        </div>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          version="1.1"
          width="160px"
          height="160px"
        >
          <defs>
            <linearGradient id="GradientColor">
              <stop offset="0%" stop-color="#e91e63" />
              <stop offset="100%" stop-color="#673ab7" />
            </linearGradient>
          </defs>
          <circle
            class="circl-1"
            cx="33"
            cy="33"
            r="30"
            stroke-linecap="round"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChAllenges",
};
</script>

<style lang="scss" scoped>
@import "../../global/scss/main.scss";
.Card {
  @include cardFormat;

  .challenge {
    margin-right: 20px;
    span:first-child {
      font-weight: 500;
      letter-spacing: 0.4px;
      font-size: 20px;
    }
    span:last-child {
      font-size: 15px;
      color: #959ca5;
    }
  }
  @include Circle;
}
</style>
