<template>
  <div>
    <div>
    {{ msg}}
    </div>
    <div>
      <form id="registForm">
        <div>
        <button id="regist" style="background-color:#5882FA;">とうろく</button>
        <button id="delete" style="background-color:#F78181;">とりけし</button>
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
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
