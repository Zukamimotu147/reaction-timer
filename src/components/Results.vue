<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Inhumane Reactions!";
    } else if (this.score < 400) {
      this.rank = "Good Reflexes";
    } else {
      this.rank = "SLOW AF";
    }
  },
};
</script>

<style>
.rank {
  font-size: 2rem;
  color: #0faf87;
  font-weight: 900;
}
</style>
