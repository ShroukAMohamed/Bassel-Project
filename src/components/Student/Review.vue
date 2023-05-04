<template>
  <div>
    <div
      class="modal fade"
      id="reviewModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header border-0">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <div class="modal-card ps-sm-5 pe-sm-5">
              <div class="d-flex justify-content-center">
                <img
                  class="img-fluid"
                  src="../../assets/352434_rate_review_icon.png"
                  alt=""
                /><span class="ms-2 fw-bold text-center">Review Course</span>
              </div>
              <form action="">
                <div class="mt-5 mb-4">
                  <div class="Rate d-flex">
                    <span>Rate it</span>
                    <div @mouseover="Rate" class="Stars ms-3">
                      <span> <i class="fa-solid fa-star"></i></span>
                      <span> <i class="fa-solid fa-star"></i></span>
                      <span> <i class="fa-solid fa-star"></i></span>
                      <span> <i class="fa-solid fa-star"></i></span>
                      <span> <i class="fa-solid fa-star"></i></span>
                    </div>
                  </div>
                  <textarea
                    name=""
                    id=""
                    cols="30"
                    rows="8"
                    required
                  ></textarea>
                  <div class="d-flex justify-content-center mt-4">
                    <input
                      type="submit"
                      value="Submit"
                      class="pb-2 pt-2 rounded-5"
                    />
                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ReviewPopup",
  methods: {
    Rate() {
      const stars = document.querySelectorAll(".Stars span");
      stars.forEach((star, index1) => {
        star.addEventListener("click", () => {
          stars.forEach((star, index2) => {
            index1 >= index2
              ? star.classList.add("active")
              : star.classList.remove("active");
          });
        });
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 800px;
  .modal-card {
    div:first-child {
      span {
        font-size: 23px;
        letter-spacing: 1px;
      }
    }
    .Rate {
      border: 1px solid rgb(118, 118, 118);
      padding: 14px 30px;
      border-radius: 30px;
      margin-bottom: 30px;

      span {
        color: #515661;
        font-size: 18px !important;
      }
      .Stars {
        span {
          color: #e6e6e6;
          cursor: pointer;
          transition: color 0.2s;
          margin-left: 5px;
        }
        span.active {
          color: #ff9c1a;
        }
      }
    }
    textarea {
      width: 100%;
      border-radius: 30px;
      padding: 30px;
      color: #515661;
      font-size: 16px;
      letter-spacing: 2px;
      resize: none;
      &:focus {
        outline: none;
      }
    }
    input {
      width: 100%;
      max-width: 200px;
      font-size: 18px;
      margin-bottom: 10px;
      background-color: #2e2a41;
      box-shadow: 0px 3px 6px #2923417a;
      color: white;
      border: 0px;
    }
  }
}
</style>
