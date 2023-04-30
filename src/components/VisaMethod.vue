<template>
  <div>
    <div
      class="modal fade"
      id="secondModal"
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
            <div class="modal-card d-flex justify-content-center">
              <div class="edit-card">
                <div class="d-flex justify-content-center align-items-center">
                  <img src="../assets/payment_icon.png" alt="" />
                  <span>Add Card</span>
                </div>
                <div class="mt-5">
                  <p>CARD NUMBER</p>
                  <div class="card-number d-flex">
                    <input id="number" type="text" />
                    <div class="d-flex align-items-center">
                      <img src="../assets/visa_card.png" alt="" />
                    </div>
                  </div>
                </div>
                <div class="card-name mt-4">
                  <p>CARDHOLDER NAME</p>
                  <input type="text" />
                </div>
                <div class="expire-cvv d-flex mt-4 pb-4">
                  <div>
                    <p>EXPIRE DATE</p>
                    <input id="expire" type="text" />
                  </div>
                  <div>
                    <p>CVV</p>
                    <input id="cvv" type="text" />
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="modal-footer d-flex justify-content-center">
            <button
              type="button"
              class="btn btn-primary w-50 rounded-5 pt-2 pb-2"
              data-bs-target="#exampleModal"
              data-bs-toggle="modal"
              data-bs-dismiss="modal"
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
export default {
  name: "VisaMethod",
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 800px;
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
      div {
        .card-number {
          input {
            width: 100%;
            max-width: 200px;
            &:focus {
              outline: none;
            }
          }
          div {
            border: 1px solid #bce0fd;
            padding: 0 15px;
            border-radius: 5px;
            margin-left: 10px;
          }
        }
      }
      .card-name {
        input {
          width: 100%;
          max-width: 300px;
        }
      }
      .expire-cvv {
        div:first-child {
          input {
            width: 100%;
            max-width: 100px;
          }
        }
        div:last-child {
          margin-left: 10px;
          input {
            width: 100%;
            max-width: 60px;
          }
        }
      }
    }
  }
}
</style>
