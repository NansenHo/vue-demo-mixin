<template>
  <div>Child1</div>
</template>

<script>
export default {
  data(){
    return {
      name: 'Child1',
      time: undefined
    }
  },
  created(){
    this.time = new Date()
    console.log(`${this.name} was born`);
  },
  beforeDestroy() {
    const now = new Date()
    console.log(`${this.name} died, and it has ${now - this.time}ms life`);
  }
}
</script>