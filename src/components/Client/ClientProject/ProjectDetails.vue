<template>
  <div class="Card-inside">
    <div class="content">
      <div class="d-flex justify-content-between">
        <span>{{ Milestone_title }}</span>
        <span>{{ Status }}</span>
      </div>
      <div class="d-lg-flex justify-content-between">
        <span class="d-block"
          ><span><i class="fa-solid fa-calendar-days"></i></span>
          {{ ProjDate }}</span
        >
        <span><i class="fa-solid fa-wallet"></i> {{ ProjSalary }}</span>
      </div>
      <p>
        {{ Details }}
      </p>
      <span><i class="fa-solid fa-comments"></i> Comments & Replies</span>
      <p class="text-center mt-2">
        comment and replies disappear after 2 months
      </p>
      <div class="comments">
        <p>
          {{ Comment }}
        </p>
        <div class="line"></div>
        <p class="mt-2">Reply</p>
        <p>
          {{ Reply }}
        </p>
        <div class="text-end">
          <span> {{ comment_date }} </span>
        </div>
      </div>
      <div class="mt-3 mb-3">
        <p class="mb-0">Leave a comment</p>
        <div class="d-flex justify-content-between align-items-end">
          <input type="text" />
          <span>Send</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectDetails",
  props: [
    "Milestone_title",
    "Status",
    "ProjDate",
    "ProjSalary",
    "Details",
    "Comment",
    "Reply",
    "comment_date",
  ],
};
</script>

<style lang="scss" scoped>
@import "../../global/scss/main.scss";
.Card-inside {
  background-color: white;
  padding: 15px;
  @include insideCard;
}
</style>
