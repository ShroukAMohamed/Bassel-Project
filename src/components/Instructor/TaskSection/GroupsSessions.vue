<template>
  <div class="GroupCard d-flex flex-column flex-lg-row align-items-center">
    <div class="col-lg-5">
      <img
        class="img-fluid"
        src="../../../assets/undraw_social_friends_re_7uaa.svg"
        alt=""
      />
    </div>
    <div class="col-lg-7 mt-4 mt-lg-0">
      <h3 class="text-center">Group 1 ( Front-End )</h3>
      <div class="d-flex justify-content-center align-items-center Sessions">
        <span @click="prevSessions" class="text-primary me-3">
          <i class="fa-solid fa-circle-chevron-left Left Hide"></i>
        </span>
        <div class="text-center ms-2 me-2 session active">
          <div class="mt-4">
            <button class="me-3 btn btn-outline-primary">Session 1</button>
            <button class="btn btn-outline-primary">Session 2</button>
          </div>
          <div class="mt-4">
            <button class="me-3 btn btn-outline-primary">Session 3</button>
            <button class="btn btn-outline-primary">Session 4</button>
          </div>
          <div class="mt-4">
            <button class="me-3 btn btn-outline-primary">Session 5</button>
            <button class="btn btn-outline-primary">Session 6</button>
          </div>
        </div>
        <div class="text-center session Hidden">
          <div class="mt-4">
            <button class="me-3 btn btn-outline-primary">Session 7</button>
            <button class="btn btn-outline-primary">Session 8</button>
          </div>
          <div class="mt-4">
            <button class="me-3 btn btn-outline-primary">Session 9</button>
            <button class="btn btn-outline-primary">Session 10</button>
          </div>
          <div class="mt-4">
            <button class="me-3 btn btn-outline-primary">Session 11</button>
            <button class="btn btn-outline-primary">Session 12</button>
          </div>
        </div>
        <span @click="nextSessions" class="text-primary ms-3">
          <i class="fa-solid fa-circle-chevron-right Right"></i>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";
export default {
  name: "GroupsSessions",
  mounted() {
    this.checkSlider();
  },
  methods: {
    checkSlider() {
      if ($(".Sessions > div.session:first-of-type").hasClass("Hidden")) {
        $(".Left").removeClass("Hide");
      } else {
        $(".Left").addClass("Hide");
      }

      if ($(".Sessions > div.session:last-of-type").hasClass("Hidden")) {
        $(".Right").removeClass("Hide");
      } else {
        $(".Right").addClass("Hide");
      }
    },
    nextSessions() {
      var com = this;
      $(".session.active").fadeOut(300, function () {
        $(this)
          .next(".session")
          .addClass("active")
          .removeClass("Hidden")
          .fadeIn();
        $(this).addClass("Hidden").removeClass("active");
        com.checkSlider();
      });
    },
    prevSessions() {
      var com = this;
      $(".session.active").fadeOut(300, function () {
        $(this)
          .prev(".session")
          .addClass("active")
          .removeClass("Hidden")
          .fadeIn();
        $(this).addClass("Hidden").removeClass("active");
        com.checkSlider();
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.GroupCard {
  background-color: white;
  box-shadow: 0px 3px 15px #00000029;
  border-radius: 10px;
  padding-top: 25px;
  padding-bottom: 35px;
  .Hidden {
    display: none;
  }
  .Hide {
    display: none;
  }
  > div:nth-child(2) {
    span:first-child,
    span:last-child {
      font-size: 28px;
      cursor: pointer;
    }
    > div:nth-child(2) {
      > div {
        button {
          padding-top: 4px;
          padding-bottom: 4px;
        }
      }
    }
  }
}
</style>
