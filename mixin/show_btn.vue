<script>
import $ from "jquery";
export default {
  methods: {
    showFunction(ClassName, btnName1, btnName2) {
      $(ClassName).fadeIn();
      $(btnName1).hide();
      $(btnName2).show();
    },
    hideFunction(ClassName, btnName1, btnName2) {
      $(ClassName).fadeOut();
      $(btnName1).show();
      $(btnName2).hide();
    },
  },
};
</script>
