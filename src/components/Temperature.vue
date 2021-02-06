<template>
  <div>
    <div class="box-temp">
      <h4 class="text-black temp-header">Temperature:</h4>
      <div class="descriptions">
        <div class="desc">
          <div class="desc-icons">
            <span class="dotted-circle bg-red">
              <span></span>
            </span>
          </div>
          <div class="desc-text">
            <span>Internal:</span>
            <span class="value">24</span>
          </div>
        </div>
        <div class="desc desc-right">
          <div class="desc-icons">
            <span class="dotted-circle bg-black">
              <span></span>
            </span>
          </div>
          <div class="desc-text">
            <span>External:</span>
            <span class="value">15</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.desc-icons {
  .bg-red {
    border: 2px solid $main-black;

    span {
      background: $primary-color;
    }
  }

  .bg-black {
    border: 2px solid $primary-color;

    span {
      background: $main-black;
    }
  }
}

.dotted-circle {
  width: 1rem;
  height: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 1000px;
}

.dotted-circle span {
  width: 0.4rem;
  height: 0.4rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 999px;
}

.box-temp {
  .desc {
    display: flex;
    align-items: center;

    &-right {
      margin-left: 2rem;
    }

    &-text {
      margin-left: 0.75rem;
    }
  }

  .value {
    margin-left: 0.45rem;
    position: relative;
  }

  .value::after {
    content: "";
    position: absolute;
    top: 0;
    right: -10;
    width: 0.35rem;
    height: 0.35rem;
    border-radius: 9999px;
    border: 1px solid $main-black;
  }
}

.descriptions {
  display: flex;
  align-items: center;
}
</style>