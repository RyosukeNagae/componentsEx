<template>
  <div class="human">
    <div class="atama">
      <div v-if="isLaughing">🤣</div>
      <div v-else>😊</div>
    </div>
    <div
      class="karada"
      @click="
        makeLaugh();
        changeCloth();
      "
    >
      <div>💪{{ body[clothNum] }}💪</div>
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
      type: [],
      default: ["👕"],
    },
  },
  data() {
    return {
      isLaughing: false,
      clothNum: 0,
    };
  },
  methods: {
    makeLaugh() {
      this.isLaughing = true;
    },
    changeCloth() {
      const len = this.body.length;
      if (this.clothNum < len - 1) {
        this.clothNum++;
      } else {
        this.clothNum = 0;
      }
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
