<template>
  <div class="Card-3">
    <div class="d-flex justify-content-center align-items-center pt-4">
      <div class="skill">
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
      <div class="challenge">
        <span class="d-block">Challenge 01</span>
        <span>XX of total XX</span>
      </div>
    </div>
    <div class="line"></div>
    <div class="d-flex justify-content-center align-items-center pt-4">
      <div class="skill">
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
            class="circl-2"
            cx="33"
            cy="33"
            r="30"
            stroke-linecap="round"
          />
        </svg>
      </div>
      <div class="challenge">
        <span class="d-block">Challenge 02</span>
        <span>XX of total XX</span>
      </div>
    </div>
    <div class="line"></div>
    <div class="d-flex justify-content-center align-items-center pt-4 pb-4">
      <div class="skill">
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
            class="circl-3"
            cx="33"
            cy="33"
            r="30"
            stroke-linecap="round"
          />
        </svg>
      </div>
      <div class="challenge">
        <span class="d-block">Challenge 03</span>
        <span>XX of total XX</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PeRcentage",
};
</script>

<style lang="scss" scoped>
@import "../../global/scss/main.scss";
.Card-3 {
  @include cardFormat;
  text-align: center;
  h4 {
    font-size: 18px;
    padding-top: 22px;
  }

  @include Circle;
  .line {
    @include lineFormat;
    margin-top: 8px !important;
  }
  .challenge {
    text-align: start;
    margin-left: 5px;
    span:first-child {
      font-weight: 500;
      letter-spacing: 0.4px;
      font-size: 20px;
    }
    span:last-child {
      font-size: 13px;
      color: #7c828a;
    }
  }
}
</style>
