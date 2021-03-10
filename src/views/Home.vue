<template>
  <div class="home">
    <!-- <img id="logo" alt="Vue logo" src="../assets/logo.png" /> -->
    <QuizCard />
  </div>
</template>

<script>
// @ is an alias to /src
import QuizCard from "@/components/QuizCard.vue";

export default {
  name: "Home",
  components: {
    QuizCard,
  },
};
</script>

<style scoped lang="scss">
#logo {
  width: 140px;
  margin: 40px 0;
}
</style>
