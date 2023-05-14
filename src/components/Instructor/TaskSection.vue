<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-8">
        <GroupsSessions />
        <GroupsSessions class="mt-5" />
        <GroupsSessions class="mt-5" />
      </div>
      <div class="col-lg-4 gy-5 gy-lg-0">
        <div class="StudentCard pt-4 pb-4 mb-4">
          <h4 class="text-center">
            Session State
            <span class="ms-2 text-success"
              ><i class="fa-solid fa-pen-to-square"></i
            ></span>
          </h4>
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
          <StudentTask />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import StudentTask from "./TaskSection/StudentsTasks.vue";
import GroupsSessions from "./TaskSection/GroupsSessions.vue";
export default {
  name: "TaskSection",
  components: { GroupsSessions, StudentTask },
};
</script>

<style lang="scss" scoped>
.StudentCard {
  background-color: rgba(217, 204, 204, 0.156);
  box-shadow: 0px 3px 8px #00000029;
  border-radius: 10px;
  width: 100%;
  margin: auto;
  height: 100%;
  max-height: 900px;
  overflow: auto;
}
</style>
