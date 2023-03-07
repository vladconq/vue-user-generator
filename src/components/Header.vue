<template>
  <header>
    <h1>Task Tracker</h1>
    <Button v-show="homePage" @click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" />
  </header>
</template>

<script>
import Button from '@/components/Button'

export default {
  name: 'Header',
  props: {
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
  computed: {
    homePage() {
      if(this.$route.path === '/') {
        return true
      } else {
        return false
      }
    }
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
