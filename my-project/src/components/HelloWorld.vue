<!--
 * @Author: RenLe
 * @Date: 2020-10-12 16:55:40
 * @LastEditors: RenLe
 * @LastEditTime: 2020-10-12 17:02:05
 * @Description: file content
 * @FilePath: /my-project/src/components/HelloWorld.vue
-->
<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: String,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
