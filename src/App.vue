<template>
  <fast-design-system-provider use-defaults>
    <fast-card>
      <HelloWorld :msg="msg"/>
      <fast-text-field
        appearance="filled"
        placeholder="Write something here"
        :modelValue="msg"
        @update:modelValue="msg = $event"
        @input:modelValue="msg = $event"
      >
        Just saying hello!
      </fast-text-field>
    </fast-card>
  </fast-design-system-provider>
</template>

<script>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  setup() {
    const msg = ref('Just saying hello')
    return {
      msg,
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
