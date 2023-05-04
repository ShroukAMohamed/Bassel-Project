<template>
  <div>
    <section id="Contact" class="contact-form block">
      <div class="contact-img d-flex align-items-center">
        <div class="container">
          <div class="row justify-content-center pt-4 pb-4">
            <div class="col-12">
              <div
                data-aos="fade-in"
                data-aos-duration="1000"
                class="form-card pt-4 pb-5 ps-3 pe-3"
              >
                <h2 class="text-center">
                  Our Dear Customer, Feel Free To Contact With Us
                </h2>
                <form action="">
                  <div class="d-flex flex-column">
                    <input type="text" placeholder="Full Name" required />
                    <input type="text" placeholder="Phone Number" required />
                    <input type="text" placeholder="Email" required />
                    <input type="text" placeholder="Location" required />

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
                      required
                      placeholder="Description"
                      name=""
                      id=""
                      cols="30"
                      rows="4"
                    ></textarea>
                    <input class="border-0" type="submit" />
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
        font-family: "Poppins", sans-serif;
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

      input[type="submit"] {
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
        transition: all 0.3s;
        &:hover {
          transform: translateY(-5px);
        }
      }
    }
  }
}
</style>
