<!--
 * @Author: RenLe
 * @Date: 2020-10-12 16:55:40
 * @LastEditors: RenLe
 * @LastEditTime: 2020-10-12 17:19:50
 * @Description: file content
 * @FilePath: /my-project/src/views/Home.vue
-->
<template>
  <div class="home">
    <HelloWorld msg="home"/>
  </div>
  <h1>{{count}}</h1>
  <h1>{{double}}</h1>
  <button @click="increase">+1</button>
</template>

<script lang="ts">
import { computed, defineComponent,ref } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

export default defineComponent({
  name: 'Home',
  components: {
    HelloWorld,
  },
  setup(){
    // ref 是一个函数，它接受一个参数，返回的就是一个神奇的 响应式对象 。我们初始化的这个 0 作为参数包裹到这个对象中去，在未来可以检测到改变并作出对应的相应。
    const count = ref(0)
    const double = computed(()=> {
      return count.value * 2
    })
    const increase = (()=> {
      count.value++
    })
    return {
      count,
      increase,
      double
    }
  }
});

</script>
