<template>
  <div id="app">
    <div class="box">
      <span class="version">Version 312.ca</span>
      <h3 class="sub-header text-black">Status</h3>

      <div class="main-content">
        <div>
          <ProgressBar />
        </div>
        <div class="stats">
          <div class="temp">
            <Temperature />
          </div>
          <div class="car-status">
            <CarStatus />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CarStatus from "./components/CarStatus";
import ProgressBar from "./components/ProgressBar";
import Temperature from "./components/Temperature";

export default {
  name: "App",
  components: { CarStatus, ProgressBar, Temperature },
};
</script>

<style lang="scss">
#app {
  display: flex;
  align-items: center;
  padding: 10rem 2rem;
  justify-content: center;
}

.text-black {
  color: $main-black;
}

.box {
  position: relative;
  width: 44rem;
  border: 4px solid $primary-color;
  border-radius: 10px;
  padding: 1.25rem 1rem;
}

.version {
  position: absolute;
  top: 5px;
  right: 20px;
  font-size: 0.75rem;
  font-weight: 500;
  color: $grey;
}
.sub-header {
  border-bottom: 2px solid $line;
  font-weight: 600;
  margin-bottom: 3rem;
}

.main-content {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}

.car-status {
  margin-top: 2rem;
}
</style>
