<script>
export default {
  methods: {
    hideModal(model_name) {
      // const myModal = new bootstrap.Modal.getInstance("#exampleModal");
      // document.querySelector(".add-card").addEventListener("click", () => {
      //   myModal.hide();
      // });
      const myModal = bootstrap.Modal.getInstance(model_name);
      myModal.hide();
    },
  },
};
</script>
