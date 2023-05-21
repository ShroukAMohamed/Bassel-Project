<template>
  <div>
    <div
      class="modal fade"
      id="SeeTaskModal"
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
                  src="../../../assets/352275_cloud_download_icon_32.png"
                  alt=""
                /><span class="ms-2 fw-bold text-center">Download Task</span>
              </div>
              <form action="">
                <div class="d-flex justify-content-center mt-4">
                  <input
                    type="button"
                    value="Download"
                    class="pb-2 pt-2 mt-4 mb-5 btn btn-secondary rounded-5"
                  />
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
  name: "SeeTask",
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 400px;
  .modal-card {
    div:first-child {
      span {
        font-size: 25px;
        letter-spacing: 1px;
      }
    }

    input {
      width: 100%;
      max-width: 180px;
      font-size: 16px;
      margin-bottom: 10px;
    }
  }
}
</style>
