<template>
  <div class="human">
    <div class="atama">
      <div v-if="isLaughing">🤣</div>
      <div v-else>😊</div>
    </div>
    <div class="karada" v-on:click="makeLaugh">
      <div>💪{{ body }}💪</div>
    </div>
    <div class="ashi">
      <div>🦵🦵</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    body: {
      type: String,
      default: "👕",
    },
  },
  data() {
    return {
      isLaughing: false,
    };
  },
  methods: {
    makeLaugh() {
      this.isLaughing = true;
    },
  },
};
</script>

<style>
.human {
  width: 10rem;
  font-size: 3rem;
  text-align: center;
}
</style>
