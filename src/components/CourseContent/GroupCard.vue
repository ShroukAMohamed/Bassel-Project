<template>
  <div class="col-xl-5 col-12">
    <div class="Card pt-4 pb-4 ps-sm-4 pe-sm-4 mt-3 mb-2">
      <h4><i class="fa-solid fa-users"></i> Group Title</h4>
      <span class="">Offline</span>
      <div class="dates">
        <span>From: <span>01/30</span></span>
        <span>To: <span>10/30</span></span>
        <span>Duration: <span>10 Days</span></span>
      </div>
      <p class="attendance">Days of Attendance: per week</p>
      <div class="d-flex justify-content-between Time">
        <div class="d-flex flex-column align-items-center">
          <span>Mon</span> <span>12:1 pm</span>
        </div>

        <div class="d-flex flex-column align-items-center">
          <span>Teus</span> <span>12:1 pm</span>
        </div>

        <div class="d-flex flex-column align-items-center">
          <span>Mon</span> <span>12:1 pm</span>
        </div>

        <div class="d-flex flex-column align-items-center">
          <span>Teus</span> <span>12:1 pm</span>
        </div>

        <div class="d-flex flex-column align-items-center">
          <span>Teus</span> <span>12:1 pm</span>
        </div>
      </div>
      <div class="location">
        <p>Location: <span>Armenia, Cape Town</span></p>
        <p>
          Max Capacity: <span>100 enrollment</span>
          <span>40 Available</span>
        </p>
      </div>
      <div class="line-2"></div>
      <div class="line-3">
        <div class="track-title">
          <p><i class="fa-solid fa-laptop-code"></i> Track Title</p>
          <p>
            Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor.
            Morbi in nibh
          </p>
        </div>
        <div class="track-topics">
          <p class="text-center">12 Track Topics</p>
          <p>1. Lorem, ipsum dolor.</p>
          <p>1. Lorem, ipsum dolor.</p>
          <p>1. Lorem, ipsum dolor.</p>
          <p>1. Lorem, ipsum dolor.</p>
          <p>1. Lorem, ipsum dolor.</p>
          <p>1. Lorem, ipsum dolor.</p>
          <p>1. Lorem, ipsum dolor.</p>
          <p>1. Lorem, ipsum dolor.</p>
        </div>
      </div>
      <div class="line-4">
        <p><i class="fa-solid fa-laptop-code"></i> Track Title</p>
        <p>
          Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor.
          Morbi in nibh
        </p>
      </div>
      <div class="d-flex justify-content-center">
        <router-link to="/Enroll">Enroll Now</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GroupCard",
};
</script>

<style lang="scss" scoped>
.Card {
  background-color: white;
  width: 100%;
  max-width: 450px;
  margin: auto;
  border-radius: 10px;
  position: relative;
  &::after {
    content: "1000 EGP";
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    width: 130px;
    height: 50px;
    padding-left: 20px;
    background-color: #ffb12b;
    color: white;
    font-weight: bold;
    top: 3.5%;
    right: 0%;
    clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 25% 100%, 0% 50%);
  }
  h4 {
    font-size: 19px;
    font-weight: bold;
    letter-spacing: 1px;
  }
  span:first-of-type:not(.dates span, .Time span, p span) {
    font-size: 18px;
    color: rgb(80, 78, 78);
    font-weight: 500;
    letter-spacing: 0.5px;
  }
  .dates {
    padding-top: 5px;
    span {
      font-size: 17px;
      color: rgb(80, 78, 78);
      font-weight: 300;
      letter-spacing: 1px;
      padding-right: 6px;
      span {
        font-weight: 500;
        font-size: 16px;
      }
    }
  }
  .attendance {
    font-size: 18px;
    color: rgb(109, 108, 108);
    font-weight: 300;
    letter-spacing: 1px;
    margin: 5px 0;
  }
  .Time {
    div {
      position: relative;
      &:not(:first-child):after {
        content: "";
        position: absolute;
        margin: 0 5px;
        height: 40px;
        left: -20%;
        top: 10%;
        border-left: 1.5px solid rgb(161, 160, 160);
      }
      span:first-of-type {
        font-size: 18px;
        color: rgb(118, 117, 117);
        font-weight: 400;
        letter-spacing: 1px;
      }
      span:last-of-type {
        font-size: 14px;
        font-weight: 600;
      }
    }
  }
  .location {
    p {
      margin: 10px 0;
      font-size: 18px;
      font-weight: 300;
      letter-spacing: 0.5px;
      color: rgb(71, 70, 70);
      span {
        color: rgb(88, 87, 87);
        font-weight: 500;
        font-size: 17px;
      }
    }
    p:last-child {
      span:last-child {
        color: #e57989;
        font-weight: 400;
        margin-left: 8px;
      }
    }
  }
  .line-2 {
    border-bottom: 0.8px solid rgb(154, 154, 154);
    padding-top: 2px;
  }
  .line-3 {
    position: relative;
    margin-left: 13px;
    &::before {
      content: "";
      position: absolute;
      width: 3.5px;
      height: 100%;
      background-color: #2596be;
      top: 5%;
      left: -4%;
    }
    .track-title {
      padding-top: 10px;
      p:first-child {
        font-weight: 500;
        font-size: 18px;
        color: black;
        margin-bottom: 5px;
        letter-spacing: 0.8px;
      }
      p:last-child {
        color: #515661;
        font-size: 17px;
        font-weight: 300;
        letter-spacing: 1px;
        margin-left: 15px;
      }
    }
    .track-topics {
      background-color: #cfcfcf63;
      padding: 10px;
      padding-bottom: 15px;
      height: 175px;
      width: 95%;
      margin: auto;
      overflow: auto;
      p {
        color: #515661;
      }
      p:first-child {
        font-weight: 300;
      }
      p:not(:first-child) {
        margin: 8px 0;
        text-align: center;
      }
    }
  }

  .line-4 {
    position: relative;
    margin-left: 13px;
    margin-top: 30px;
    &::before {
      content: "";
      position: absolute;
      width: 3.5px;
      height: 100%;
      background-color: #4bc50f;
      top: 5%;
      left: -4%;
    }

    padding-top: 10px;
    p:first-child {
      font-weight: 500;
      font-size: 18px;
      color: black;
      margin-bottom: 5px;
      letter-spacing: 0.8px;
    }
    p:last-child {
      color: #515661;
      font-size: 17px;
      font-weight: 300;
      letter-spacing: 1px;
      margin-left: 15px;
    }
  }

  a {
    border: 0;
    width: 75%;
    margin: 15px 0;
    padding: 10px 0;
    background-color: #6864b9;
    box-shadow: 0px 3px 6px #6864b969;
    color: white;
    text-decoration: none;
    text-align: center;
  }
}
</style>
