<template>
  <div>
    <div>
    {{ msg}}
    </div>
    <div>
      <form id="registForm">
        <div>
        <button type="button"
          v-on:click="regist('success')"
          style="background-color:#5882FA;">とうろく
        </button>
        <button type="button"
          v-on:click="regist('failed')"
          style="background-color:#F78181;">とりけし
        </button>
        </div>
        <select name="なまえ" id="who">
          <option value="-">-</option>
          <option value="さくや">さくや</option>
          <option value="もとき">もとき</option>
        </select>
        <select name="なにを" id="what">
          <option value="-">-</option>
          <option value="あそび">あそび</option>
          <option value="べんきょう">べんきょう</option>
        </select>
        <input type="time" id="time" placeholder="じかんをにゅうりょくしてください。">
      </form>
      <div class="action-list">
        <label class="action-list__item">
          <input type="checkbox"><button>EDIT</button>vue-r
        </label>
        <label class="action-list__item">
          <input type="checkbox"><button>EDIT</button>vuex
        </label>
        <label class="action-list__item">
          <input type="checkbox"><button>EDIT</button>vue-loader
        </label>
        <label class="action-list__item--checked">
          <input type="checkbox" checked><button>EDIT</button>awesome-vue
        </label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Styles learned by my sons.',
    };
  },
  methods: {
    regist(msg2) {
      console.log(msg2);
    },
  },
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
.action-list {
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
