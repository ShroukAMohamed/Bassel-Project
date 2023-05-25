<template>
  <div>
    <div
      class="modal fade"
      id="cancelModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <form action="">
            <div class="modal-body mb-4">
              <div class="modal-card d-flex justify-content-center">
                <div class="edit-card">
                  <div class="d-flex justify-content-center align-items-center">
                    <img
                      src="../../../assets/clock_decoration_time_icon.png"
                      alt=""
                    />
                    <span>Change Date</span>
                  </div>
                  <div class="card-name mt-4 ms-3">
                    <p>Add A New Date</p>
                    <input type="date" required />
                  </div>
                </div>
              </div>
            </div>
            <div class="modal-footer d-flex justify-content-center">
              <input
                type="submit"
                value="Request"
                class="btn btn-primary rounded-5 pt-2 pb-2 mt-2 mb-2"
              />
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import Swal from "sweetalert2";
// import $ from "jquery";
export default {
  name: "CancelModal",
  // methods: {
  //   SweetAlert() {
  //     Swal.fire({
  //       position: "top-end",
  //       icon: "success",
  //       title: "Your work has been saved",
  //       showConfirmButton: false,
  //       timer: 1500,
  //     });
  //   },
  // },
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 500px;
  .modal-card {
    span {
      font-size: 30px;
      font-weight: 500;
      margin-left: 5px;
      letter-spacing: 1px;
    }
    p {
      margin-bottom: 5px;
    }
    .edit-card {
      input {
        padding: 10px;
        border-radius: 5px;
        font-size: 14px;
        border: 1px solid rgb(170, 169, 169);
        &:focus {
          outline: none;
        }
      }
      p {
        font-size: 12px;
        color: #676666;
        font-weight: 500;
      }

      .card-name {
        input {
          width: 100%;
        }
      }
    }
  }
  .modal-footer {
    input {
      width: 100%;
      max-width: 180px;
    }
  }
}
</style>
