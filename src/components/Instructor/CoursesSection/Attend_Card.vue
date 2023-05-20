<template>
  <div class="SmallCard mt-4">
    <div class="d-flex justify-content-around align-items-center">
      <div class="d-flex align-items-center">
        <img class="img-fluid me-3" src="../../../assets/cheif1.jpg" alt="" />
        <span>Shon Smith</span>
      </div>
      <div class="studentCheck d-flex align-items-center">
        <input type="checkbox" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Attend_Card",
};
</script>

<style lang="scss" scoped>
.SmallCard {
  background-color: white;
  box-shadow: 0px 3px 15px #00000029;
  padding: 12px 0;
  border-radius: 20px;
  width: 100%;
  max-width: 380px;
  margin: auto;
  img {
    position: relative;
    top: 0;
    left: 0;
    width: 42px;
    object-fit: cover;
    height: 42px;
    border-radius: 50%;
  }
  .studentCheck {
    input {
      width: 17px;
      height: 17px;
      cursor: pointer;
    }
  }
}
</style>
