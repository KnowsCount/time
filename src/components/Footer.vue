<template>
  <footer>
    <h3>share your thoughts to help us improve!</h3>
    <div class="center">
      <FeedbackReactions />
    </div>
    <br />
    <code
      >don't worry, we respect your privacy, so your result will not be sent to
      us.</code
    >
  </footer>
</template>

<script>
import FeedbackReactions from "./FeedbackReactions.vue";
export default {
  components: {
    FeedbackReactions,
  },
};
</script>

<style>
footer {
  font-family: -apple-system, "Helvetica Neue", sans-serif, Arial, Helvetica;
  position: absolute;
  right: 0;
  bottom: 0;
  left: 0;
  /* background-color: #efefef; */
  text-align: center;
}
li {
  display: inline;
  list-style: none;
  padding: 5px 5px;
}
code {
  background-color: #e5e5f7;
}
.center {
  /* padding-left: 38.5%; */
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
