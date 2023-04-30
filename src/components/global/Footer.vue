<template>
  <div class="footer">
    <div class="container h-100">
      <div class="row align-items-center justify-content-center pt-5">
        <div class="col-lg-4 col-12 d-flex d-lg-block justify-content-center">
          <img src="../../assets/Full-Logo.png" alt="" />
        </div>
        <div
          class="col-lg-4 col-12 text-center text-sm-start d-flex justify-content-center gy-5 gy-lg-0"
        >
          <div>
            <p class="fw-bold">Quick Access</p>
            <p>Home</p>
            <p>Customer / Contact Us</p>
            <p>Courses</p>
            <p>Login</p>
          </div>
        </div>
        <div
          class="col-lg-4 col-12 text-center text-sm-start d-flex justify-content-center gy-5 gy-lg-0"
        >
          <div>
            <p class="fw-bold">Others</p>
            <p>Privacy Policy</p>
            <p>Terms of Conditions</p>
            <p>About Us</p>
          </div>
        </div>
      </div>
      <div class="row pt-5 pb-5">
        <div class="col-12 text-center fw-bold copyright">
          Copy Right Reserved <i class="fa-solid fa-copyright"></i> Bassel Allam
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterA",
};
</script>

<style scoped lang="scss">
.footer {
  margin-top: 20px;
  background-color: #7f7bd4;
  color: white;
  .copyright {
    letter-spacing: 1px;
  }
  p:not(:first-of-type) {
    font-weight: 400;
    transition: all 0.3s;
    cursor: pointer;
    color: rgb(228, 228, 228);
    &:hover {
      color: white;
    }
  }
  p:first-of-type {
    letter-spacing: 1px;
  }
}
</style>
