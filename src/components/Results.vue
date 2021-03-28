<template>
  <p style="color:green">Reaction time - {{ score }} ms</p>
  <h3 style="color:tomato">Your Rank</h3>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank : null
    }
  },
  mounted() {
    if (this.score < 225) {
      this.rank = 'INSANE'
    } else if (this.score < 300) {
      this.rank = 'SHARP'
    }else if (this.score < 400) {
      this.rank = 'GOOD'
    }else {
      this.rank = 'Please Concentrate'
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.5em;
    color: purple;
    font-weight: bold;
  }
</style>