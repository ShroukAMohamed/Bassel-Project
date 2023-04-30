<template>
  <div>
    <div
      class="modal fade"
      id="exampleModal"
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
            <div class="modal-card">
              <div
                class="d-flex justify-content-center align-items-center pb-4"
              >
                <img src="../assets/payment_icon.png" alt="" />
                <span>Payment</span>
              </div>
              <div class="bg-course">
                <p>Project Name</p>
              </div>
              <form action="">
                <div class="method">
                  <!-- <div
                    class="d-flex justify-content-between align-items-center cash-border"
                  >
                    <div>
                      <input id="vodafone" name="pay" type="radio" />
                      <label for="vodafone">Vodafone Cash - فودافون كاش</label>
                    </div>
                    <img src="../../assets/cash.png" alt="" />
                  </div> -->
                  <!-- <div
                    class="d-flex justify-content-between align-items-center cash-border"
                  >
                    <div>
                      <input id="fawry" name="pay" type="radio" />
                      <label for="fawry">Fawry - فوري</label>
                    </div>
                    <img src="../../assets/cash.png" alt="" />
                  </div> -->
                  <div
                    class="d-flex justify-content-between align-items-center cash-border"
                  >
                    <div>
                      <input id="cash" name="pay" type="radio" />
                      <label for="cash">Cash - كاش</label>
                    </div>
                    <img src="../assets/cash.png" alt="" />
                  </div>
                  <div
                    class="d-flex justify-content-between align-items-center cash-border"
                  >
                    <div>
                      <input id="visa" name="pay" type="radio" />
                      <label for="visa">Visa or Credit Card</label>
                      <input
                        class="d-block add-card"
                        type="button"
                        value="Add A Card"
                        data-bs-toggle="modal"
                        data-bs-target="#secondModal"
                        @click="hideModal('#exampleModal')"
                      />
                    </div>
                    <img src="../assets/cash.png" alt="" />
                  </div>
                </div>
              </form>
            </div>
          </div>
          <div
            class="modal-footer border-0 d-flex justify-content-center mt-4 mb-5"
          >
            <button
              type="button"
              class="btn btn-primary w-50 pb-2 pt-2 rounded-5"
              data-bs-target="#thirdModal"
              data-bs-toggle="modal"
              data-bs-dismiss="modal"
              @click="hideModal('#exampleModal')"
            >
              Confirm
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import hide_model from "../../mixin/hide_model.vue";
export default {
  name: "PaymentComponent",
  mixins: [hide_model],
};
</script>

<style lang="scss" scoped>
@import "./global/scss/main.scss";
.modal-dialog {
  max-width: 800px;

  .modal-card {
    span {
      font-size: 30px;
      font-weight: 500;
      margin-left: 20px;
      letter-spacing: 1px;
    }
    .bg-course {
      background-color: #edecec;
      padding: 15px 0;
      margin: 15px 0;
      position: relative;
      &::before {
        content: "1000 EGP";
        position: absolute;
        right: 0;
        color: white;
        padding: 18px 0;
        padding-left: 40px;
        padding-right: 15px;
        font-weight: 600;
        top: 0;
        clip-path: polygon(25% 0%, 100% 0%, 100% 100%, 25% 100%, 0% 50%);
        background-color: #ffb12b;
        @include breakpoints(mobile) {
          font-size: 15px;
          padding-top: 16px;
          padding-bottom: 16px;
        }
      }
      p {
        margin-bottom: 0;
        margin-left: 15px;
        font-weight: bold;
        font-size: 20px;
        letter-spacing: 1.5px;
        @include breakpoints(mobile) {
          font-size: 17px;
          letter-spacing: normal;
        }
      }
    }

    .method {
      .cash-border {
        width: 100%;
        margin: auto;
        border: 0.8px solid black;
        margin-top: 25px;
        padding: 15px 35px;
        border-radius: 25px;
        @include breakpoints(mobile) {
          padding: 8px 15px;
        }

        input[type="radio"] {
          position: relative;
          appearance: none;
          &:checked + label::after,
          &:not(:checked):hover + label::after {
            content: "";
            position: absolute;
            background-color: black;
            border-radius: 50%;
            width: 10px;
            height: 10px;
            left: 3px;
            top: 10px;
            @include breakpoints(mobile) {
              top: 7px;
            }
          }
          &:not(:checked):hover + label::after {
            opacity: 0.2;
          }
        }
        label {
          position: relative;
          padding-left: 25px;
          letter-spacing: 1px;
          font-size: 20px;
          @include breakpoints(mobile) {
            font-size: 16px;
          }
          &::before {
            content: "";
            position: absolute;
            border-radius: 50%;
            width: 16px;
            height: 16px;
            border: 1px solid black;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            background-color: white;
          }
        }
        .add-card {
          background-color: transparent;
          color: #1c03c5;
          text-decoration: underline;
          margin-left: 18px;
          font-weight: 500;
          border: 0;
        }
      }
    }
    input[type="submit"]:not(.method input) {
      color: white;
      font-size: 18px;
      background: #2699fb;
      border-radius: 25px;
      width: 60%;
      border: 0;
      box-shadow: 0px 3px 6px #2923417a;
      padding: 10px 50px;
    }
  }
}
</style>
