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
    <div class="pt-2 pb-3">
      <div class="d-flex align-items-center ps-4 pe-3">
        <div>
          <p>{{ Course_Name }}</p>
          <p>
            <span>{{ Session_Num }}</span> sessions
          </p>
          <p>{{ Completion }} completed</p>
        </div>
        <img class="img-fluid ms-3" src="../../assets/wavy-line.png" alt="" />
      </div>
      <div class="line"></div>
      <div class="TrackDetails ps-4 pe-4">
        <div class="d-flex justify-content-between mt-2">
          <p>{{ TrackInfo }}</p>
          <span><i class="fa-solid fa-laptop-code"></i></span>
        </div>
        <p>{{ TrackDetails }}</p>
        <div class="d-flex justify-content-between">
          <p>{{ Group }}</p>
          <span><i class="fa-solid fa-users"></i></span>
        </div>
        <p class="fw-semibold">{{ GroupStatus }}</p>
        <div class="d-flex flex-column flex-sm-row">
          <div>
            <span>From:</span>
            <span>{{ FromDate }}</span>
          </div>
          <div>
            <span>To:</span>
            <span>{{ ToDate }}</span>
          </div>
          <div>
            <span>Duration:</span>
            <span>{{ Duration }}</span>
          </div>
        </div>
        <div>
          <p>
            Location: <span>{{ CourseLocation }}</span>
          </p>
          <p>
            Max Capacity: <span>{{ MaxCapacity }}</span>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoursesOwned",
  props: [
    "Course_Name",
    "Session_Num",
    "Completion",
    "TrackInfo",
    "TrackDetails",
    "Group",
    "GroupStatus",
    "FromDate",
    "ToDate",
    "Duration",
    "CourseLocation",
    "MaxCapacity",
  ],
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
    .line {
      border-bottom: 1px solid rgb(206, 205, 205);
    }
    .TrackDetails {
      div:nth-of-type(1),
      div:nth-of-type(2) {
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
      div:nth-of-type(3) {
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
      div:last-of-type {
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
}
</style>
