<template>
  <div class="footer">
    <div class="container h-100">
      <div class="row align-items-center justify-content-center pt-5">
        <div class="col-md-4 col-12 d-flex d-lg-block justify-content-center">
          <img src="../../assets/Full-Logo.png" alt="" />
        </div>
        <div
          class="col-md-4 col-12 text-center text-md-start d-flex justify-content-center gy-5 gy-lg-0"
        >
          <div class="d-flex flex-column">
            <p class="fw-bold">Quick Access</p>
            <a href="/#Home">Home</a>
            <a href="/#Contact">Customer / Contact Us</a>
            <a href="/#Courses">Courses</a>
            <a href="/#Home">Login</a>
          </div>
        </div>
        <div
          class="col-md-4 col-12 text-center text-md-start d-flex justify-content-center gy-5 gy-lg-0"
        >
          <div class="d-flex flex-column">
            <p class="fw-bold">Others</p>
            <a>Privacy Policy</a>
            <a>Terms of Conditions</a>
            <a href="/#About">About Us</a>
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
  a {
    font-weight: 400;
    transition: all 0.3s;
    cursor: pointer;
    margin: 5px 0;
    color: rgb(235, 233, 233) !important;
    text-decoration: none;
    &:hover {
      color: white !important;
    }
  }
  p:first-of-type {
    letter-spacing: 1px;
  }
}
</style>
