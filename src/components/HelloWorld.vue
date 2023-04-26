<script setup>
import { ref } from 'vue';

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <button @click="changeWeather">点击切换天气</button>
    <h2>今天天气是{{ info }}</h2>

    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>

  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>
<script>
export default {
  name: 'School',
  data() {
    return {
      isHot: true,
    };
  },
  computed: {
    info() {
      return this.isHot ? '凉爽' : '炎热';
    },
  },
  methods: {
    changeWeather() {
      this.isHot = !this.isHot;
    },
  },
};
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
