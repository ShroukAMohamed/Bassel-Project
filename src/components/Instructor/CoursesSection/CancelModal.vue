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
                <div class="card-name mt-4">
                  <p>Add A New Date</p>
                  <input type="date" required />
                </div>
              </div>
            </div>
          </div>
          <div class="modal-footer d-flex justify-content-center">
            <button
              type="button"
              class="btn btn-primary w-50 rounded-5 pt-2 pb-2"
              data-bs-dismiss="modal"
            >
              Submit
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CancelModal",
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 500px;
  .modal-card {
    span {
      font-size: 30px;
      font-weight: 500;
      margin-left: 20px;
      letter-spacing: 1px;
    }
    p {
      margin-bottom: 5px;
    }
    .edit-card {
      input {
        padding: 10px;
        border: 1px solid #bce0fd;
        color: #2699fb;
        border-radius: 5px;
        font-size: 14px;
        &:focus {
          outline: none;
        }
      }
      p {
        font-size: 12px;
        color: #2699fb;
        font-weight: bold;
      }

      .card-name {
        input {
          width: 100%;
          max-width: 300px;
        }
      }
    }
  }
}
</style>
