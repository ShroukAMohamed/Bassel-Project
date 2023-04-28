<template>
  <div class="Card">
    <div
      class="review-icon"
      data-bs-target="#reviewModal"
      data-bs-toggle="modal"
      data-bs-dismiss="modal"
    ></div>
    <img
      class="img-fluid"
      src="../../assets/mr-bochelly-IBKyH0V3rew-unsplash_copy.png"
      alt=""
    />
    <div class="p-4 pt-2">
      <div class="d-flex align-items-center">
        <div>
          <p>Course Title here</p>
          <p><span>20/50</span> sessions</p>
          <p>60 % completed</p>
        </div>
        <img class="img-fluid" src="../../assets/wavy-line.png" alt="" />
      </div>
      <div class="line"></div>
      <div class="d-flex justify-content-between mt-2">
        <p>Track Info</p>
        <span><i class="fa-solid fa-laptop-code"></i></span>
      </div>
      <p>Mauris imperdiet orci dapibus, commodo libero nec, interdum</p>
      <div class="d-flex justify-content-between">
        <p>Group</p>
        <span><i class="fa-solid fa-users"></i></span>
      </div>
      <p class="fw-semibold">Offline</p>
      <div class="d-flex flex-column flex-sm-row">
        <div>
          <span>From:</span>
          <span>01/30</span>
        </div>
        <div>
          <span>To:</span>
          <span>10/30</span>
        </div>
        <div>
          <span>Duration:</span>
          <span>10 Days</span>
        </div>
      </div>
      <div>
        <p>Location: <span>Armenia, Cape Town</span></p>
        <p>Max Capacity: <span>100 enrollment</span></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoursesOwned",
};
</script>

<style lang="scss" scoped>
.Card {
  width: 100%;
  max-width: 460px;
  padding: 0 !important;
  margin: auto !important;
  margin-top: 30px !important;
  .review-icon {
    position: relative;
    &::before {
      content: "";
      position: absolute;
      background-image: url("../../assets/352434_rate_review_icon_24.png");
      background-repeat: no-repeat;
      background-position: center center;
      width: 45px;
      height: 40px;
      background-color: white;
      border-top-right-radius: 15px;
      right: 0;
      cursor: pointer;
    }
  }
  img {
    border-top-left-radius: 15px;
    border-top-right-radius: 15px;
  }

  div {
    div:first-child {
      p:first-of-type {
        font-size: 17px;
        letter-spacing: 0.5px;
        margin-bottom: 3px;
      }
      p:nth-of-type(2) {
        font-size: 17px;
        margin-bottom: 3px;
        letter-spacing: 0.5px;
        span {
          font-size: 20px;
        }
      }
      p:nth-of-type(3) {
        color: #ff2366;
        font-weight: 300;
        font-size: 14px;
      }
      img {
        width: 20%;
        margin-left: 5px;
        height: 35%;
      }
    }
    div:nth-child(3),
    div:nth-child(5) {
      p {
        font-weight: 600;
        font-size: 18px;
        letter-spacing: 1px;
        margin-bottom: 5px;
      }
      + p {
        color: gray;
        font-size: 16px;
        letter-spacing: 1px;
        width: 100%;
        max-width: 300px;
      }
      span {
        color: #515661;
        font-size: 20px;
      }
    }
    div:nth-child(7) {
      div {
        margin-right: 15px;
        margin-bottom: 10px;
        span {
          color: #515661;
          font-size: 16px;
          font-weight: 300;
          letter-spacing: 1px;
          word-break: break-all;
        }
        span:last-of-type {
          font-weight: 500;
        }
      }
    }
    div:last-child {
      p {
        color: #515661;
        font-size: 16px;
        font-weight: 300;
        letter-spacing: 1px;
        span {
          font-weight: 500;
        }
      }
    }
  }
}
</style>
