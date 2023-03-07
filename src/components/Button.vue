<template>
  <button @click="onClick()" class="btn">{{ text }}</button>
</template>

<script>
export default {
  name: 'Button',
  methods: {
    onClick() {
      console.log('click')
    },
  },
  props: {
    text: String,
  },
}
</script>
