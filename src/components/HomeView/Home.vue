<template>
  <div class="bg-img">
    <transition name="fade" appear>
      <div
        class="modal-overlay position-fixed"
        v-if="showModal"
        @click="showModal = false"
      ></div>
    </transition>
    <transition name="slide" appear>
      <div
        class="modal position-fixed"
        @click="showModal = false"
        v-if="showModal"
      >
        <div class="row w-100 h-100">
          <div class="col-12 h-100 d-flex align-items-center">
            <div class="modal-card" @click.stop>
              <div class="text-end mt-3 me-3" @click="showModal = false">
                <button type="button" class="btn-close ps-1"></button>
              </div>
              <div>
                <div
                  class="d-flex flex-column flex-sm-row text-center align-items-center justify-content-center"
                >
                  <img src="../../assets/locked.png" alt="" />
                  <span class="ms-sm-3 mt-3 mt-sm-0">Login As :-</span>
                </div>
                <form class="mt-sm-5 mt-4" @submit.prevent="student_dashboard">
                  <input class="d-block" type="submit" value="Student" />
                </form>
                <form @submit.prevent="client_dashboard">
                  <div class="d-flex justify-content-center mt-4 mb-4">
                    <input type="submit" value="Client" />
                  </div>
                </form>

                <form @submit.prevent="instructor_dashboard">
                  <div class="d-flex justify-content-center mb-5">
                    <input type="submit" value="Instructor" />
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </transition>

    <section class="h-100 block" id="Home">
      <div class="container h-100">
        <div class="row align-items-center justify-content-center h-100">
          <div
            data-aos="zoom-out"
            data-aos-duration="1000"
            data-aos-delay="800"
            class="col-md-6 d-flex d-lg-block flex-column align-items-center"
          >
            <div class="d-flex flex-column flex-sm-row align-items-center">
              <div class="bassel-img d-none d-md-block"></div>
              <h2 class="ps-md-2 fw-bold">BASSEL ALLAM</h2>
            </div>
            <p class="ps-md-2 pt-3 text-center text-md-start">
              Vivamus eget aliquam dui. Integer eu arcu vel
            </p>
            <div
              class="mt-5 d-flex flex-column w-100 align-items-center align-items-md-start"
            >
              <button @click="showModal = true">Login</button>
            </div>
          </div>
          <div
            data-aos="fade-in"
            data-aos-duration="1000"
            class="col-md-6 order-md-last order-first d-flex justify-content-center gy-5 gy-sm-0"
          >
            <img class="img-fluid" src="../../assets/Logo-Png.png" alt="" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "HomeComponent",
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    student_dashboard() {
      this.$router.push("/Student");
    },
    client_dashboard() {
      this.$router.push("/Client");
    },
    instructor_dashboard() {
      this.$router.push("/Instructor");
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../components/global/scss/main.scss";
.bg-img {
  position: relative;
  background-image: url("../../assets/Group282_edit2.png");
  width: 100%;
  height: 100vh;
  background-size: cover;
  background-position: 100% 100%;
  @include breakpoints(mobile) {
    height: 100%;
    padding-bottom: 30px;
  }

  .modal {
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    z-index: 99;
    .modal-card {
      background-color: white;
      width: 100%;
      max-width: 500px;
      border-radius: 30px;
      margin: auto;
      border: 0.8px solid black;
      > div:first-child {
        cursor: pointer;
      }
      span {
        font-size: 30px;
        font-weight: 600;
        font-family: "poppins", serif;
        letter-spacing: 1px;
      }

      input[type="submit"] {
        border: 0;
        font-size: 19px;
        border: 1px solid #2537e0;
        color: #2537e0;
        box-shadow: 0px 3px 6px #2923417a;
        text-decoration: none;
        padding: 10px 0;
        margin: auto;
        border-radius: 25px;
        background-color: transparent;
        background-color: white;
        text-align: center;
        width: 100%;
        max-width: 250px;
        transition: all 0.3s;
        &:hover {
          transform: scale(1.1);
        }
      }
    }
  }
  .modal-overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 98;
    background-color: #01010145;
  }
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.5s;
  }

  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }
  .slide-enter-active,
  .slide-leave-active {
    transition: transform 0.8s;
  }

  .slide-enter,
  .slide-leave-to {
    transform: translateY(-100%);
  }

  .bassel-img {
    background-image: url("../../assets/Logo-Png.png");
    width: 85px;
    height: 85px;
    background-size: cover;
  }
  h2 {
    font-family: "Bebas Neue", cursive;
    font-size: 44px;
    margin-bottom: 0;
    letter-spacing: 1px;
  }
  p {
    font-size: 28px;
    font-weight: 600;
    letter-spacing: 1px;
    width: 100%;
    max-width: 400px;
    @include breakpoints(mobile) {
      font-size: 22px;
    }
  }

  button:not(.btn-close) {
    border: 0;
    background-color: transparent;
    letter-spacing: 1px;
    font-size: 20px;
    color: whitesmoke;
    background: transparent linear-gradient(180deg, #2596be 0%, #2503f3) 0% 0%
      no-repeat padding-box;
    opacity: 1;
    box-shadow: 0px 3px 6px #292341;
    padding: 10px 0;
    transition: all 0.3s;
    &:hover {
      transform: translateY(-4px);
    }
    border-radius: 28px;
    width: 100%;
    max-width: 250px;
    @include breakpoints(mobile) {
      font-size: 16px;
      width: 80%;
    }
  }
}
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap");
</style>
