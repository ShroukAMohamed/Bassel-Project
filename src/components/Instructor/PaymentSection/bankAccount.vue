<template>
  <div>
    <div
      class="modal fade"
      id="AccountModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-4">
          <div class="modal-header">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <form action="">
            <div class="modal-body">
              <div class="modal-card d-flex justify-content-center pb-3">
                <div class="edit-card">
                  <div class="d-flex justify-content-center align-items-center">
                    <img
                      src="../../../assets/bank_card_checkout_online_payment method_icon.png"
                      alt=""
                    />
                    <span>Add Account</span>
                  </div>
                  <div class="BankCard mt-4">
                    <p>ACCOUNT NUMBER</p>
                    <input type="text" required />
                  </div>
                  <div class="BankCard mt-4">
                    <p>BANK NAME</p>
                    <input type="text" required />
                  </div>
                  <div class="BankCard mt-4">
                    <p>IBAN NUMBER</p>
                    <input type="text" required />
                  </div>
                </div>
              </div>
            </div>
            <div class="modal-footer">
              <input
                type="submit"
                value="Change"
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
export default {
  name: "VisaMethod",
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 500px;
  .modal-card {
    span {
      font-size: 26px;
      font-weight: 500;
      margin-left: 15px;
      letter-spacing: 1px;
      font-family: "Poppins", serif;
    }
    p {
      margin-bottom: 5px;
    }
    .edit-card {
      width: 100%;
      max-width: 300px;
      margin: auto;
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

      .BankCard {
        input {
          width: 100%;
        }
      }
    }
  }
  .modal-footer {
    input {
      width: 100%;
      max-width: 200px;
      margin: auto;
    }
  }
}
</style>
