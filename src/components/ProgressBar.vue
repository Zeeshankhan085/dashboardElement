<template>
  <!-- <div class="progress-bar">
    <progress-bar :options="options" :value="90" />
  </div> -->
  <div>
    <div id="container">
      <div class="insideDiv">
        <img src="../assets/img/battery.png" alt="" />
        <span class="charge-text"> {{ currentCharge }}% </span>
        <div class="distance">
          <img src="../assets/img/distance.png" alt="" />
          <span>550KM</span>
        </div>
      </div>
      <p class="text-status">Full in: 25 min.</p>
    </div>
  </div>
</template>

<script>
var ProgressBar = require("progressbar.js");

export default {
  components: {},
  mounted() {
    var bar = new ProgressBar.Circle(document.getElementById("container"), {
      strokeWidth: 8,
      easing: "easeInOut",
      duration: 1400,
      color: "#19df40",
      trailColor: "#d1f9d9",
      trailWidth: 8,
      svgStyle: null,
    });
    bar.animate(this.currentCharge / 100);
  },
  data() {
    return {
      currentCharge: 90,
    };
  },
};
</script>

<style lang="scss">
.progress-bar {
  padding: 2rem;
  /* background: #000; */
}

#container {
  margin: 20px;
  width: 200px;
  height: 8px;
  margin-top: -1rem;
  position: relative;
  transform: translateX(-20px);
}

.insideDiv {
  position: absolute;
  transform: translate(65px, 30px);
  display: flex;
  padding-top: 1rem;
  flex-direction: column;
  align-items: center;

  .charge-text {
    margin-top: 0.5rem;
    font-size: 1.25rem;
  }

  .distance {
    margin-top: 0.75rem;
    display: flex;
    align-items: center;

    span {
      margin-left: 0.5rem;
    }
  }
}

.text-status {
  position: absolute;
  transform: translate(40px, 210px);
}
</style>