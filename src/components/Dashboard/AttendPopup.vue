<template>
  <div>
    <div
      class="modal fade"
      id="attendModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header border-0 d-block text-end">
            <div class="ps-3 pe-3">
              <div class="w-100">
                <button
                  type="button"
                  class="btn-close"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                ></button>
              </div>
              <div
                class="d-flex flex-column flex-sm-row justify-content-sm-between justify-content-center align-items-center"
              >
                <p class="Attend-header text-start">Course Attendance</p>
                <div
                  class="d-flex justify-content-center justify-content-sm-end pt-3"
                >
                  <div class="me-3 text-start">
                    <p><span>20/50</span> sessions</p>
                    <span>60% completed</span>
                  </div>
                  <img
                    class="img-fluid"
                    src="../../assets/wavy-line.png"
                    alt=""
                  />
                </div>
              </div>
              <div class="header-line"></div>
            </div>
          </div>
          <div class="modal-body">
            <div class="modal-card ps-3 pe-3 pb-5">
              <div class="Courses-time d-flex">
                <span class="active"
                  ><i class="fa-solid fa-circle-check"></i
                ></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span class="active"
                  ><i class="fa-solid fa-circle-check"></i
                ></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span class="active"
                  ><i class="fa-solid fa-circle-check"></i
                ></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span><i class="fa-solid fa-circle-check"></i></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span><i class="fa-solid fa-circle-check"></i></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div
      class="modal fade"
      id="secondModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header border-0 d-block text-end">
            <div class="ps-3 pe-3">
              <div class="w-100">
                <button
                  type="button"
                  class="btn-close"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                ></button>
              </div>
              <div
                class="d-flex flex-column flex-sm-row justify-content-sm-between justify-content-center align-items-center"
              >
                <p class="Attend-header text-start">Course Attendance</p>
                <div
                  class="d-flex justify-content-center justify-content-sm-end pt-3"
                >
                  <div class="me-3 text-start">
                    <p><span>20/50</span> sessions</p>
                    <span>60% completed</span>
                  </div>
                  <img
                    class="img-fluid"
                    src="../../assets/wavy-line.png"
                    alt=""
                  />
                </div>
              </div>
              <div class="header-line"></div>
            </div>
          </div>
          <div class="modal-body">
            <div class="modal-card ps-3 pe-3 pb-5">
              <div class="Courses-time d-flex">
                <span class="active"
                  ><i class="fa-solid fa-circle-check"></i
                ></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span class="active"
                  ><i class="fa-solid fa-circle-check"></i
                ></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span class="active"
                  ><i class="fa-solid fa-circle-check"></i
                ></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span class="active"
                  ><i class="fa-solid fa-circle-check"></i
                ></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
                </div>
              </div>
              <div class="Courses-time d-flex">
                <span><i class="fa-solid fa-circle-check"></i></span>
                <div class="ms-3">
                  <span> Session Title goes here</span>
                  <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
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
  name: "AttendPopup",
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 750px;
  .modal-header {
    .header-line {
      border-bottom: 1px solid rgb(194, 191, 191);
      margin-top: 10px;
    }

    img {
      width: 20%;
    }
    .Attend-header {
      font-size: 20px !important;
      font-weight: bold;
      letter-spacing: 1.5px;
    }

    div {
      p:first-of-type {
        font-size: 17px;
        margin-bottom: 1px;
        span {
          font-size: 18px;
        }
      }
      span:nth-child(2) {
        color: #ff2366;
        font-weight: 300;
        font-size: 13px;
      }
    }
  }
  .modal-body {
    .Courses-time {
      > span {
        font-size: 20px;
        color: #5156618f;
      }
      span.active {
        color: #309100;
      }
      div {
        span {
          color: #4a505d;
          font-size: 18px;
        }
        p {
          color: #515661;
          font-size: 18px;
          span {
            color: #010101;
            font-size: 14px;
          }
        }
      }
    }
  }
}
</style>
