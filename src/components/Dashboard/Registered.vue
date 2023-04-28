<template>
  <div>
    <div class="form-card mt-5 mb-5">
      <h3 class="pt-3 pb-2 ms-5">Your Registered Info</h3>
      <div class="line"></div>
      <form action="">
        <div class="d-flex flex-column mt-5 mb-5">
          <p class="text-center mb-0">
            " These Data Can't Be Edited Or Changed "
          </p>
          <div
            class="Input ps-md-5 d-flex justify-content-between align-items-center"
          >
            <input disabled type="text" placeholder="Full Name" /><i
              class="fa-solid fa-user"
            ></i>
          </div>
          <div
            class="Input ps-md-5 d-flex justify-content-between align-items-center"
          >
            <input disabled type="text" placeholder="Email" /><i
              class="fa-solid fa-envelope"
            ></i>
          </div>
          <div
            class="Input ps-md-5 d-flex justify-content-between align-items-center"
          >
            <input disabled type="text" placeholder="Phone Number" /><i
              class="fa-solid fa-phone"
            ></i>
          </div>
          <div
            class="Input ps-md-5 d-flex justify-content-between align-items-center"
          >
            <input disabled type="text" placeholder="Detailed Address" /><i
              class="fa-solid fa-location-dot"
            ></i>
          </div>
          <div
            class="Input ps-md-5 d-flex justify-content-between align-items-center"
          >
            <input disabled type="text" placeholder="Date of birth" /><i
              class="fa-solid fa-calendar-days"
            ></i>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "RegistInfo",
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.form-card {
  background-image: white;
  box-shadow: 0px 3px 6px #2923417a;
  border-radius: 20px;
  padding-top: 10px;
  padding-bottom: 40px;
  width: 100%;
  max-width: 900px;
  margin: auto;
  h3 {
    letter-spacing: 1px;
    font-weight: 600;
    font-size: 23px;
  }
  p {
    color: #e57989;
  }
  .line {
    border-bottom: 1px solid rgb(206, 205, 205);
    width: 95%;
    margin: auto;
  }
  .Input {
    width: 90%;
    max-width: 500px;
    margin: auto;
    padding: 5px 16px;
    margin-top: 25px;
    border-radius: 25px;
    border: 0.8px solid black;
    font-size: 22px;
    @include breakpoints(mobile) {
      font-size: 16px;
      padding: 6px 16px;
    }
    input:not(input[type="radio"]) {
      border: none;
      width: 100%;
      background-color: transparent;
      &:focus {
        outline: #292341;
        outline: none;
      }
      &::placeholder {
        letter-spacing: 0.5px;
        font-size: 17px;
        @include breakpoints(mobile) {
          font-size: 15px;
          letter-spacing: normal;
        }
      }
    }
  }
}
</style>
