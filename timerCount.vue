<template>
<div>
    {{ timerCount }}
</div>
</template>
<script>
export default {
  data() {
    return {
        timerCount: 10,
    }
  },
  watch: {
    timerCount: {
        handler(value) {
            if (value > 0) {
                setTimeout(() => {
                    this.timerCount--;
                }, 10);
            }
        },
    immediate: true // This ensures the watcher is triggered upon creation
    }
  }
}

</script>