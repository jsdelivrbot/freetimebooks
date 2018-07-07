<template>
  <div id="app">
    <img src="./assets/riv0066-051.jpg" alt="title_img" width="40%" height="40%">
    <h1>じゆうじかんちょう</h1>
    <hr>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  @mixin flex-vender() {
    display: flex;
    display: -webkit-flex;
    display: -moz-flex;
    display: -ms-flex;
    display: -o-flex;
  }
  .task-list {
    @include flex-vender;
    flex-direction: column;
    align-items: center;
    &__item {
      width: 270px;
      text-align: left;
      $element: #{&};
      &--checked {
        @extend #{$element};
        color: #85a6c6;
      }
    }
  }
</style>
