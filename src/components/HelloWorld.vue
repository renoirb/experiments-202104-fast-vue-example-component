<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <fast-button appearance="accent" @click="onClick">Click Me</fast-button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  model: {
    prop: 'msg',
    event: 'change',
  },
  props: {
    msg: {
      type: String,
      default: 'Hi!',
    },
  },
  methods: {
    onClick: function () {
      console.log('clicked!');
    }
  }
}
</script>

<style scoped>
  fast-design-system-provider {
    display: block;
  }

  fast-card {
    padding: 16px;
    display: flex;
    flex-direction: column;
  }

  h2 {
    font-size: var(--type-ramp-plus-5-font-size);
    line-height: var(--type-ramp-plus-5-line-height);
  }

  fast-card > fast-button {
    align-self: flex-end;
  }
</style>
