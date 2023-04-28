<template>
  <section class="charts overflow-hidden">
    <div class="container">
      <div class="row align-items-center justify-content-center mt-4">
        <div class="col-lg-4 col-md-6 col-12 gy-5 gy-lg-0">
          <div class="Card-3 d-flex justify-content-center">
            <div>
              <h4>Chart title goes here</h4>
              <div id="chartStyle">
                <canvas id="myChart" width="150" height="150"></canvas>
              </div>
              <div class="line-3"></div>
              <div class="pt-3 pb-3 labels ps-2">
                <span>Point 01</span>
                <span>Point 02</span>
                <span>Point 03</span>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 col-12 gy-5 gy-lg-0">
          <div class="Card-3 d-flex justify-content-center">
            <div>
              <h4>Chart title goes here</h4>
              <div id="Andchart">
                <div class="Before"></div>
                <canvas id="AndChart" width="200" height="200"></canvas>
              </div>
              <div class="pt-4 pb-4 labels ps-3">
                <span>Long Category Label 01</span>
                <span>Long Category Label 02</span>
                <span>Long Category Label 03</span>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-12 col-12 gy-5 gy-lg-0">
          <Percentage />
        </div>
      </div>
      <div class="row pt-5 justify-content-center">
        <div class="col-lg-4 col-md-6 col-12 gy-5 gy-lg-0">
          <Challenges />
        </div>
        <div class="col-lg-4 col-md-6 col-12 gy-5 gy-lg-0">
          <Challenges />
        </div>
        <div class="col-lg-4 col-md-12 col-12 gy-5 gy-lg-0">
          <Challenges />
        </div>
      </div>
      <div class="row pt-5 justify-content-end pb-5">
        <div class="col-lg-4 col-md-6 col-12 gy-5 gy-lg-0">
          <div class="card-5">
            <div class="ps-4">
              <p class="pt-4">Challenge 01</p>
              <span>XX of total XX</span>
              <div class="progress">
                <div
                  class="progress-bar"
                  role="progressbar"
                  style="width: 35%"
                  aria-valuenow="35"
                  aria-valuemin="0"
                  aria-valuemax="100"
                ></div>
              </div>
              <span>XX of total XX</span>
              <div class="progress">
                <div
                  class="progress-bar"
                  role="progressbar"
                  style="width: 75%"
                  aria-valuenow="75"
                  aria-valuemin="0"
                  aria-valuemax="100"
                ></div>
              </div>
              <span>XX of total XX</span>
              <div class="progress">
                <div
                  class="progress-bar"
                  role="progressbar"
                  style="width: 65%"
                  aria-valuenow="65"
                  aria-valuemin="0"
                  aria-valuemax="100"
                ></div>
              </div>
              <div class="pb-4"></div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 col-12 gy-5 gy-lg-0">
          <div class="card-5">
            <div class="ps-4">
              <p class="mb-0 pt-4">Challenge 01</p>
              <div class="d-flex ds-progress">
                <div class="progress">
                  <div
                    class="progress-bar"
                    role="progressbar"
                    style="width: 65%"
                    aria-valuenow="65"
                    aria-valuemin="0"
                    aria-valuemax="100"
                  ></div>
                </div>
                <span>35%</span>
              </div>
              <div class="line-3 ms-0"></div>
              <div class="pt-2 pb-3">
                <span>Here go numbers XX of total XX</span>
              </div>
            </div>
          </div>
          <div class="card-6 pt-4">
            <div class="category-card d-flex justify-content-around">
              <div class="category">
                <p>354</p>
                <span>Category</span>
              </div>
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
                    cx="23"
                    cy="23"
                    r="20"
                    stroke-linecap="round"
                  />
                </svg>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 col-12 gy-5 gy-lg-0">
          <div class="card-6">
            <div class="category-card ps-3 pe-3">
              <span class="category-icon"
                ><i class="fa-solid fa-moon"></i
              ></span>
              <p>Category</p>
              <div class="ca-progress">
                <div class="progress">
                  <div
                    class="progress-bar"
                    role="progressbar"
                    style="width: 35%"
                    aria-valuenow="35"
                    aria-valuemin="0"
                    aria-valuemax="100"
                  ></div>
                </div>
              </div>
              <span>7.2h of 8h</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Chart from "chart.js/auto";
import Challenges from "./Charts/Challenges.vue";
import Percentage from "./Charts/Percentage.vue";
export default {
  name: "ChartsComponent",
  components: { Challenges, Percentage },
  mounted() {
    const ctx = document.getElementById("myChart");
    const data = {
      datasets: [
        {
          label: "Percentage",
          data: [70, 20, 15],
          backgroundColor: ["#147AD6", "#79D2DE", "#EC6666"],
          hoverOffset: 4,
          hoverBorderWidth: 0,
          offset: 0,
          borderRadius: 50,
          spacing: 8,
          cutout: 55,
        },
      ],
    };
    const myChart = new Chart(ctx, {
      type: "doughnut",
      data: data,
      options: {},
    });
    myChart;

    const ctxs = document.getElementById("AndChart");
    const datachart = {
      datasets: [
        {
          label: "Percentage",
          data: [58, 24, 26],
          backgroundColor: ["#147AD6", "#79D2DE", "#EC6666"],
          hoverOffset: 4,
          cutout: 35,
          spacing: 0,
        },
      ],
    };
    const AndChart = new Chart(ctxs, {
      type: "doughnut",
      data: datachart,
      options: {},
    });
    AndChart;
  },
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";

.charts {
  margin-top: 80px;
  .Card-3 {
    @include cardFormat;
    text-align: center;
    h4 {
      font-size: 18px;
      padding-top: 22px;
    }
    #chartStyle {
      @include Charts;
      &::before {
        content: "76%";
        position: absolute;
        font-size: 32px;
        top: 38%;
        left: 30%;
        font-weight: 300;
      }
    }
    #Andchart {
      @include Charts;
      &::before {
        content: "26%";
        position: absolute;
        font-size: 11.5px;
        top: 4%;
        left: 5%;
        @include percentage;
      }
      &::after {
        content: "54%";
        position: absolute;
        font-size: 11.5px;
        top: 45%;
        left: 80%;
        @include percentage;
      }
      .Before {
        &::before {
          content: "30%";
          position: absolute;
          font-size: 11.5px;
          top: 65%;
          left: -1%;
          @include percentage;
        }
      }
    }

    .labels {
      span {
        color: gray;
        display: block;
        font-size: 12px;
        padding: 3px 0;
        font-weight: 300;
        position: relative;
        &::before {
          content: "";
          position: absolute;
          width: 7px;
          height: 7px;
          margin-top: 5px;
          margin-left: -13px;
          border-radius: 50%;
        }
        &:nth-child(1):before {
          background-color: #147ad6;
        }
        &:nth-child(2):before {
          background-color: #ec6666;
        }
        &:nth-child(3):before {
          background-color: #79d2de;
        }
      }
    }
    .line-3 {
      @include lineFormat;
    }
  }

  .card-5 {
    @include cardFormat;
    .progress {
      width: 80%;
      height: 7.5px;
      margin: 10px 0;
    }
    .progress:nth-of-type(1) {
      .progress-bar {
        background-color: #147ad6;
      }
    }
    .progress:nth-of-type(2) {
      .progress-bar {
        background-color: #ec6666;
      }
    }
    .progress:nth-of-type(3) {
      .progress-bar {
        background-color: #79d2de;
      }
    }
    p {
      font-weight: 600;
      font-size: 20px;
      letter-spacing: 0.8px;
    }
    span {
      font-size: 15px;
      color: #8a8a8bcb;
    }
    .ds-progress {
      .progress {
        width: 68%;
        height: 8px;
        margin-top: 13px;
      }
      span {
        font-size: 20px;
        color: black;
        font-weight: 600;
        margin-left: 6px;
        margin-right: 10px;
      }
    }
    .line-3 {
      @include lineFormat;
    }
  }
  .card-6 {
    width: 90%;
    max-width: 300px;
    margin: auto;
    @include breakpoints(small) {
      max-width: 400px;
    }
    .category-card {
      background-color: white;
      box-shadow: 0 0.5rem 3rem rgba(0, 0, 0, 0.15) !important;
      border-radius: 10px;
      width: 55%;
      padding: 10px 0;
      p {
        margin-bottom: 0px;
        color: #000000;
        font-size: 22px;
        font-weight: 500;
      }
      span {
        font-size: 15px;
        color: #8a8a8bcb;
      }
      @include circleTwo;
      .ca-progress {
        .progress {
          height: 8px;
          margin-top: 10px;
          margin-bottom: 10px;
          .progress-bar {
            background-color: #147ad6;
          }
        }
      }
      .category-icon {
        font-size: 30px;
        color: #147ad6;
        padding-left: 4px;
      }
    }
  }
}
</style>
