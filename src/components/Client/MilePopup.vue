<template>
  <div>
    <div
      class="modal fade"
      id="mileModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header d-block text-end">
            <div class="ps-3 pe-3">
              <div class="w-100">
                <button
                  type="button"
                  class="btn-close"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                ></button>
              </div>
              <div class="d-flex justify-content-center align-items-center">
                <img
                  class="img-fluid"
                  src="../../assets/MaskGroup47.svg"
                  alt=""
                />
                <h3 class="mb-0 ms-3 text-start">Project Name - Milestones</h3>
              </div>
            </div>
          </div>
          <div class="modal-body d-flex d-md-block justify-content-center">
            <div
              class="modal-card d-flex flex-column-reverse flex-md-row justify-content-around mt-3 mb-5"
            >
              <div class="part-1">
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
              </div>
              <div class="Line d-none d-md-block"></div>
              <div class="part2">
                <div class="d-flex justify-content-center">
                  <img
                    class="img-fluid"
                    src="../../assets/MaskGroup53-svg.svg"
                    alt=""
                  />
                </div>

                <div class="Card-inside">
                  <div class="content">
                    <div class="d-flex justify-content-between">
                      <span>Milestone Title</span>
                      <span>Status</span>
                    </div>
                    <div class="d-lg-flex justify-content-between">
                      <span class="d-block"
                        ><span><i class="fa-solid fa-calendar-days"></i></span>
                        12 Jan - 12 Mar</span
                      >
                      <span
                        ><i class="fa-solid fa-wallet"></i> Due : 1000 EGP</span
                      >
                    </div>
                    <p>
                      Mauris imperdiet orci dapibus, commodo libero nec,
                      interdum tortor. Morbi in nibh faucibus, iaculis lorem
                      vitae, cursus velit. Etiam non
                    </p>
                    <span
                      ><i class="fa-solid fa-comments"></i> Comments &
                      Replies</span
                    >
                    <p class="text-center mt-2">
                      comment and replies disappear after 2 months
                    </p>
                    <div class="comments">
                      <p>
                        Aliquam in bibendum mauris. Sed vitae erat vel velit
                        blandit pharetra vitae nec ante. Cras at est
                      </p>
                      <div class="line"></div>
                      <p class="mt-2">Reply</p>
                      <p>
                        Aliquam in bibendum mauris. Sed vitae erat vel velit
                        blandit pharetra vitae nec ante. Cras at est
                      </p>
                      <div class="text-end">
                        <span> 12 Mar </span>
                      </div>
                    </div>
                    <div class="mt-3 mb-3">
                      <p class="mb-0">Leave a comment</p>
                      <div
                        class="d-flex justify-content-between align-items-end"
                      >
                        <input type="text" />
                        <span>Send</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MilePopup",
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.modal-dialog {
  max-width: 1200px;
  .modal-header {
    border-bottom: 1px solid rgb(173, 168, 168);
  }
  .modal-card {
    .part-1 {
      width: 100%;
      max-width: 450px;
      > div {
        background-color: white;
        box-shadow: 0px 3px 6px #00000029;
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
    }
    .Line {
      position: relative;
      margin-top: 20px;
      &::before {
        content: "";
        position: absolute;
        width: 1px;
        height: 780px;
        background-color: rgb(187, 183, 183);
      }
    }

    .part2 {
      .Card-inside {
        background-color: #dbddf738;
        box-shadow: 0px 3px 6px #00000029;
        width: 100%;
        max-width: 450px;
        padding: 10px 20px;
        @include insideCard;
      }
    }
  }
}
</style>
