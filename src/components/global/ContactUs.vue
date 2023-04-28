<template>
  <div>
    <div
      class="modal fade"
      id="contactModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header border-0 pb-0">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <div class="modal-card">
              <h3 class="text-center mb-5 mt-3">Contact Us</h3>
              <form action="">
                <textarea name="" id="" cols="30" rows="12"></textarea>
                <div class="d-flex justify-content-center mt-4">
                  <input
                    type="submit"
                    value="Submit"
                    class="pb-2 pt-2 rounded-5"
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
  name: "ContactUs",
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 700px;
  .modal-card {
    padding: 25px;
    padding-top: 0;
    h3 {
      font-size: 23px;
      font-weight: bold;
      letter-spacing: 1px;
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
      border: 0;
    }
  }
}
</style>
