<template>
  <div>
    <div
      class="modal fade"
      id="jobsModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header d-block">
            <div class="w-100 text-end">
              <button
                type="button"
                class="btn-close ms-0"
                data-bs-dismiss="modal"
                aria-label="Close"
              ></button>
            </div>
            <div class="d-flex justify-content-center align-items-center">
              <img src="../../../assets//MaskGroup47.svg" alt="" />
              <h3 class="text-center mb-0 ms-2">Apply Now</h3>
            </div>
          </div>
          <form action="">
            <div class="modal-body">
              <div class="modal-card d-flex justify-content-center">
                <div class="form-card">
                  <div class="d-flex flex-column">
                    <div
                      class="Input ps-md-5 d-flex justify-content-between align-items-center"
                    >
                      <input type="text" placeholder="Full Name" required /><i
                        class="fa-solid fa-user"
                      ></i>
                    </div>
                    <div
                      class="Input ps-md-5 d-flex justify-content-between align-items-center"
                    >
                      <input type="text" placeholder="Email" required /><i
                        class="fa-solid fa-envelope"
                      ></i>
                    </div>
                    <div
                      class="Input ps-md-5 d-flex justify-content-between align-items-center"
                    >
                      <input
                        type="text"
                        placeholder="Phone Number"
                        required
                      /><i class="fa-solid fa-phone"></i>
                    </div>
                    <div
                      class="Input ps-md-5 d-flex justify-content-between align-items-center"
                    >
                      <input
                        type="text"
                        placeholder="Detailed Address"
                        required
                      /><i class="fa-solid fa-location-dot"></i>
                    </div>
                    <div
                      class="Input ps-md-5 d-flex justify-content-between align-items-center"
                    >
                      <label class="w-100 File" for="file">CV File</label>
                      <input type="file" id="file" accept="pdf/*" required /><i
                        class="fa-solid fa-file-csv"
                      ></i>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div
              class="modal-footer d-flex justify-content-center border-0 pb-5"
            >
              <input value="enroll now" type="submit" />
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "jobsPopup",
};
</script>

<style lang="scss" scoped>
@import "../../global/scss/main.scss";
.modal-dialog {
  max-width: 800px;

  .modal-header {
    border-bottom: 0.8px solid gray;
    width: 95%;
    margin: auto;
  }
  .modal-card {
    .form-card {
      width: 100%;
      h3 {
        letter-spacing: 1px;
        font-weight: bold;
      }
      .Input {
        width: 90%;
        max-width: 500px;
        margin: auto;
        padding: 8px 16px;
        margin-top: 25px;
        border-radius: 25px;
        border: 0.8px solid black;
        font-size: 18px;
        @include breakpoints(mobile) {
          font-size: 16px;
          padding: 6px 16px;
        }
        input:not(input[type="radio"]) {
          border: none;
          width: 100%;
          &:focus {
            outline: #292341;
            outline: none;
          }
          &::placeholder {
            letter-spacing: 1.3px;
            font-size: 18px;
            @include breakpoints(mobile) {
              font-size: 15px;
              letter-spacing: normal;
            }
          }
        }
        input[type="file"] {
          display: none;
        }
        label.File {
          font-size: 18px;
          color: gray;
          font-weight: normal;
          letter-spacing: 1.3px;
          cursor: pointer;
          @include breakpoints(mobile) {
            font-size: 15px;
            letter-spacing: normal;
          }
        }
      }
    }
  }
  .modal-footer {
    input {
      border: 0;
      background-color: #6864b9;
      box-shadow: 0px 3px 6px #6864b969;
      color: white;
      width: 100%;
      max-width: 250px;
      padding: 8px 0;
    }
  }
}
</style>
