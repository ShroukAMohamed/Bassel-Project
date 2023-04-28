<template>
  <div class="Card">
    <div class="p-4">
      <div class="d-flex justify-content-between">
        <p class="mb-0">Project Name - <span>web development</span></p>
        <span class="text-center"
          ><i class="fa-solid fa-clock"></i> Status</span
        >
      </div>
      <p class="mt-2 mb-2">
        Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor.
        Morbi in nibh faucibus, iaculis lorem vitae, cursus velit.
      </p>
      <span
        ><i class="fa-solid fa-calendar-days"></i> Start Date: 1/1/2023 -
        1/1/2024</span
      >
      <div class="line mt-3"></div>
      <p class="mt-2 mb-2">Milestones 20</p>
      <div class="Card-inside">
        <div class="content">
          <div class="d-flex justify-content-between">
            <span>Milestone Title</span>
            <span>Status</span>
          </div>
          <div class="d-lg-flex justify-content-between">
            <span class="d-block"
              ><span><i class="fa-solid fa-calendar-days"></i></span> 12 Jan -
              12 Mar</span
            >
            <span><i class="fa-solid fa-wallet"></i> Due : 1000 EGP</span>
          </div>
          <p>
            Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor.
            Morbi in nibh faucibus, iaculis lorem vitae, cursus velit. Etiam non
          </p>
          <span><i class="fa-solid fa-comments"></i> Comments & Replies</span>
          <p class="text-center mt-2">
            comment and replies disappear after 2 months
          </p>
          <div class="comments">
            <p>
              Aliquam in bibendum mauris. Sed vitae erat vel velit blandit
              pharetra vitae nec ante. Cras at est
            </p>
            <div class="line"></div>
            <p class="mt-2">Reply</p>
            <p>
              Aliquam in bibendum mauris. Sed vitae erat vel velit blandit
              pharetra vitae nec ante. Cras at est
            </p>
            <div class="text-end">
              <span> 12 Mar </span>
            </div>
          </div>
          <div class="mt-3 mb-3">
            <p class="mb-0">Leave a comment</p>
            <div class="d-flex justify-content-between align-items-end">
              <input type="text" />
              <span>Send</span>
            </div>
          </div>
        </div>
      </div>
      <div class="mt-4">
        <div class="d-flex justify-content-between">
          <span>Milestone Title</span>
          <span>Status</span>
        </div>
        <div class="d-flex justify-content-between">
          <span>12 Jan - 12 Mar</span>
          <span>see more <i class="fa-solid fa-caret-down"></i></span>
        </div>
      </div>
      <button
        class="mt-4 mb-3"
        data-bs-target="#mileModal"
        data-bs-toggle="modal"
        data-bs-dismiss="modal"
      >
        Open More
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ClientProject",
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.Card {
  width: 100%;
  max-width: 460px;
  margin: auto !important;
  padding: 0 !important;
  margin-top: 30px !important;
  background-color: #f6f6f6 !important;
  box-shadow: none;
  .line {
    border-bottom: 1px solid rgb(206, 205, 205);
  }
  > div {
    > div:first-child {
      p {
        font-size: 17px;
        letter-spacing: 0.5px;
        span {
          font-weight: 300;
        }
      }
      > span {
        color: rgb(0, 156, 0);
        font-size: 17px;
      }
    }
    > p:first-of-type {
      color: #646b79;
      font-size: 18px;
      font-weight: 300;
      max-width: 450px;
      letter-spacing: 0.8px;
    }
    > span:first-of-type {
      font-size: 17px;
      font-weight: 500;
      letter-spacing: 0.5px;
    }
    > p:nth-of-type(2) {
      font-size: 18px;
      letter-spacing: 0.5px;
    }
    .Card-inside {
      background-color: white;
      padding: 15px;
      @include insideCard;
    }
    > div:last-of-type {
      background-color: white;
      padding: 10px 15px;
      > div {
        span:first-of-type {
          color: rgb(88, 87, 87);
        }
      }
      > div:first-child {
        span:first-of-type {
          font-size: 18px;
          letter-spacing: 0.5px;
        }
        span:last-of-type {
          color: #4bc50f;
        }
      }
      > div:last-child {
        span:last-of-type {
          font-size: 14px;
          cursor: pointer;
        }
      }
    }
    > button:last-child {
      border: 0;
      background-color: transparent;
      color: #6864b9;
      text-decoration: underline;
      font-weight: 600;
      letter-spacing: 0.5px;
    }
  }
}
</style>
