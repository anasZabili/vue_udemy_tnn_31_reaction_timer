<template>
  <p>Reaction time {{ reactionTime }} milliseconds</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["reactionTime"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.reactionTime < 250) {
      this.rank = "Awsome";
    } else if (this.reactionTime < 400) {
      this.rank = "Good";
    } else {
      this.rank = "Come on hurry up";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>