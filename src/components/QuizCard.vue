<template>
  <main>
    <!-- quiz section -->
    <div class="card">
      <!-- question -->
      <div class="question">
        <span class="title-card">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem iste
        </span>
      </div>
      <div class="answers">
        <div class="answer">
          <span class="answer-index">A</span
          ><span class="answer-text">Hello</span>
        </div>
        <div class="answer">
          <span class="answer-index">B</span
          ><span class="answer-text">Hello</span>
        </div>
        <div class="answer">
          <span class="answer-index">C</span
          ><span class="answer-text">Hello</span>
        </div>
        <div class="answer">
          <span class="answer-index">D</span
          ><span class="answer-text">Hello</span>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "QuizCard",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// variables
$main-color: #2879ca;

// mixin flex
@mixin flex($positionX, $positionY) {
  display: flex;
  justify-content: $positionX;
  align-items: $positionY;
}

// card style
.card {
  width: 400px;
  min-height: 500px;
  margin: auto;
  border: 1px solid $main-color;
  border-radius: 4px;
  .question {
    min-height: 100px;
    padding: 20px;
    @include flex(center, center);
    border-bottom: 1px solid $main-color;
    color: $main-color;
    background-color: $main-color;
    .title-card {
      height: 80px;
      @include flex(center, center);
      padding: 0 10px;
      border-radius: 6px;
      background-color: #fff;
    }
  }
  .answers {
    width: 100%;
    height: 400px;
    margin: auto;
    @include flex(center, center);
    flex-wrap: wrap;
    .answer {
      flex-basis: 90%;
      height: 60px;
      @include flex(space-between, center);
      margin: auto;
      .answer-index {
        width: 20%;
        height: 100%;
        color: #fff;
        @include flex(space-around, center);
        border: 1px solid $main-color;
        border-radius: 6px 0 0 6px;
        background-color: $main-color;
      }
      .answer-text {
        width: 80%;
        height: 100%;
        padding-left: 26px;
        text-align: left;
        color: $main-color;
        @include flex(start, center);
        background-color: #fff;
        border: 1px solid $main-color;
        border-radius: 0 6px 6px 0;
      }
    }
  }
}
</style>
