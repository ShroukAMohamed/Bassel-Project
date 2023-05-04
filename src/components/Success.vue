<template>
  <div>
    <div
      class="modal fade"
      id="thirdModal"
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
          <div class="modal-body">
            <div
              class="modal-card d-flex flex-column justify-content-center align-items-center"
            >
              <img class="img-fluid" src="../assets/Group286.svg" alt="" />
              <p class="text-center fw-bold">
                You Applied Successfully to the Coures You Will Have a valuable
                Learning Time
              </p>
              <button
                class="btn btn-primary w-50 rounded-5 pt-2 pb-2 mb-5"
                data-bs-dismiss="modal"
                @click="hideModal('#thirdModal')"
              >
                <router-link to="/" class=""> Back To Home </router-link>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import hide_model from "../../mixin/hide_model.vue";
export default {
  name: "SuccessComponent",
  mixins: [hide_model],
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 800px;
  .modal-card {
    p {
      font-size: 22px;
      width: 100%;
      max-width: 400px;
      margin: auto;
      letter-spacing: 1px;
      padding: 40px 0;
    }
    button {
      a {
        color: white;
        text-decoration: none;
      }
    }
  }
}
</style>
