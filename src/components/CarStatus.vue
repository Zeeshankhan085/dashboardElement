<template>
  <div>
    <h3>Car status:</h3>

    <div class="icons-container">
      <div class="icon-box">
        <img src="../assets/img/stationary.png" alt="" />
        <span>Stationary</span>
      </div>
      <div class="icon-box ml-2">
        <img src="../assets/img/locked.png" alt="" />
        <span>Locked</span>
      </div>
      <div class="icon-box ml-2">
        <img src="../assets/img/sentry.png" alt="" />
        <span>Sentry On</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
h3 {
  margin-bottom: 1rem;
  font-weight: 600;
}

.icons-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.icon-box {
  padding: 1rem 1.25rem;
  box-shadow: 4px 6px 15px -14px #000000;
  display: flex;
  width: 140px;
  flex-direction: column;
  align-items: center;
}
</style>