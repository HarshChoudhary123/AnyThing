<template>
<div style="    margin-top: 20%;
    font-size: 4rem;
    font-family: Segoe Print" >
    <div :style="mycolor">
    <center>
    ${{ timerCount }}
    </center>
</div>
</div>
</template>
<script>
export default {
  data() {
    return {
        timerCount: 1876548548680,
        mycolor: 'color: #'+(Math.random()*0xFFFFFF<<0).toString(16)
    }
  },
  watch: {
    timerCount: {
        handler(value) {
            if (value > 0) {
                setTimeout(() => {
                    this.timerCount = this.timerCount - 37845763;
                    this.mycolor = 'color: #'+(Math.random()*0xFFFFFF<<0).toString(16);
                }, 1);
            }
        },
    immediate: true // This ensures the watcher is triggered upon creation
    }
  }
}

</script>
