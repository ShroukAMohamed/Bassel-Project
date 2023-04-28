<template>
  <div>
    <section class="contact-form">
      <div class="contact-img d-flex align-items-center">
        <div class="container">
          <div class="row justify-content-center pt-4 pb-4">
            <div class="col-12">
              <div class="form-card pt-4 pb-5 ps-3 pe-3">
                <h2 class="text-center">
                  Our Dear Customer, Feel Free To Contact With Us
                </h2>
                <form action="">
                  <div class="d-flex flex-column">
                    <input type="text" placeholder="Full Name" />
                    <input type="text" placeholder="Phone Number" />
                    <input type="text" placeholder="Email" />
                    <input type="text" placeholder="Location" />

                    <div class="Selection d-flex justify-content-center">
                      <select name="" id="">
                        <option selected disabled>Required Service</option>
                        <option value="Option 1">Option 1</option>
                        <option value="Option 2">Option 2</option>
                        <option value="Option 3">Option 3</option>
                        <option value="Option 4">Option 4</option>
                      </select>
                    </div>

                    <textarea
                      placeholder="Description"
                      name=""
                      id=""
                      cols="30"
                      rows="4"
                    ></textarea>
                    <button class="border-0">Submit</button>
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "ContactComponent",
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
%inputForm {
  width: 100%;
  max-width: 450px;
  margin: auto;
  padding: 13px 50px;
  margin-top: 25px;
  border-radius: 25px;
  border: 0.8px solid black;
  @include breakpoints(mobile) {
    padding: 8px 50px;
  }
  &:focus {
    outline: none;
  }
}
.contact-form {
  margin: 50px 0;

  .contact-img {
    background-image: url("../../assets/Group281.svg");
    width: 100%;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 70% 100%;
    .form-card {
      background-image: white;
      box-shadow: 0 0.5rem 3rem rgba(0, 0, 0, 0.15) !important;
      border-radius: 20px;
      width: 100%;
      max-width: 700px;
      margin: auto;

      h2 {
        width: 100%;
        max-width: 500px;
        margin: auto;
        padding-bottom: 20px;
        padding-top: 20px;
        letter-spacing: 1px;
        font-weight: 600;
      }
      input {
        @extend %inputForm;
      }
      textarea {
        @extend %inputForm;
        resize: none;
      }

      .Selection {
        position: relative;
        width: 100%;
        max-width: 450px;
        margin: auto;
        &::before {
          content: "\f0dd";
          font-family: fontAwesome;
          position: absolute;
          top: 48%;
          right: 8%;
          pointer-events: none;
        }
        select {
          width: 100%;
          padding: 13px 50px;
          color: gray;
          margin-top: 25px;
          border-radius: 25px;
          appearance: none;
          cursor: pointer;
          &:focus {
            outline: none;
          }
          @include breakpoints(mobile) {
            padding: 8px 50px;
          }
        }
      }

      button {
        width: 100%;
        max-width: 200px;
        margin: auto;
        margin-top: 50px;
        padding: 10px 0;
        box-shadow: 0px 3px 6px #2923417a;
        border-radius: 22px;
        color: white;
        letter-spacing: 1px;
        background-color: #292341;
      }
    }
  }
}
</style>
