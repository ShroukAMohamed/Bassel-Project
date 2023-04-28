<template>
  <div>
    <div class="form-card mt-5">
      <h3 class="text-center pt-3 pb-2">Enroll Now</h3>
      <form action="">
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
            <input type="text" placeholder="Phone Number" required /><i
              class="fa-solid fa-phone"
            ></i>
          </div>
          <div
            class="Input ps-md-5 d-flex justify-content-between align-items-center"
          >
            <input type="text" placeholder="Detailed Address" required /><i
              class="fa-solid fa-location-dot"
            ></i>
          </div>
          <div
            class="Input ps-md-5 d-flex justify-content-between align-items-center"
          >
            <input type="text" placeholder="Date of birth" required /><i
              class="fa-solid fa-calendar-days"
            ></i>
          </div>
          <div class="Gender ps-md-5 d-flex justify-content-between">
            <span>Gender</span>
            <div class="d-inline">
              <input id="male" type="radio" name="same" required />
              <label class="" for="male">Male</label>
            </div>
            <div class="d-inline">
              <input name="same" id="female" type="radio" required />
              <label class="ms-2" for="female">Female</label>
            </div>
          </div>
          <div class="input-btn">
            <input
              data-bs-toggle="modal"
              data-bs-target="#exampleModal"
              type="submit"
              value="Enroll"
              @click.prevent
            />
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "enrollForm",
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.form-card {
  background-image: white;
  border: 1px solid black;
  border-radius: 20px;
  padding: 30px 0;
  h3 {
    letter-spacing: 1px;
    font-weight: bold;
  }
  .Input {
    width: 90%;
    max-width: 450px;
    margin: auto;
    padding: 10px 16px;
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
        font-size: 17px;
        @include breakpoints(mobile) {
          font-size: 15px;
          letter-spacing: normal;
        }
      }
    }
  }
  .Gender {
    width: 90%;
    max-width: 450px;
    margin: auto;
    border: 0.8px solid black;
    margin-top: 25px;
    padding: 13px 16px;
    border-radius: 25px;
    @include breakpoints(mobile) {
      padding: 9px 16px;
    }
    span {
      color: gray;
      letter-spacing: 1.3px;
      @include breakpoints(mobile) {
        font-size: 15px;
        letter-spacing: normal;
      }
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
        top: 7px;
      }
      &:not(:checked):hover + label::after {
        opacity: 0.2;
      }
    }
    label {
      position: relative;
      padding-left: 25px;
      letter-spacing: 1px;
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
  }

  .input-btn {
    display: flex;
    justify-content: center;
    input {
      width: 100%;
      max-width: 200px;
      margin: 50px auto;
      padding: 10px 0;
      box-shadow: 0px 3px 6px #2923417a;
      border-radius: 22px;
      color: white;
      border: 0;
      background-color: #292341;
      letter-spacing: 1px;
    }
  }
}
</style>
