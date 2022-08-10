<template>
  <div class="container">
    <Human />
    <Human :body="bodies" />
    <Human :body="bodies" />
  </div>
  <!-- <div>
    <simple-memo bgColor="orange">オレンジ</simple-memo>
    <simple-memo bgColor="pink">ピンク</simple-memo>
    <simple-memo bgColor="green">みどり</simple-memo>
  </div> -->
</template>

<script>
import Human from "@/components/Human.vue";
// import SimpleMemo from "./components/SimpleMemo.vue";

export default {
  components: {
    Human,
    // SimpleMemo,
  },
  data() {
    return {
      bodies: ["👕", "👗", "🧥"],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
}
</style>
