<template>
  <div class="decision-card">
    <div class="decision-card-content">
      <h3>{{ topic }}</h3>
      <span class="subtitle">Think more about it</span>
      <div class="decision-progress-bars">
        <span class="progress-bar">
          <span
            class="progress-bar-fill progress-bar-pros"
            :style="{ width: progressPros + '%' }"
          ></span>
        </span>
        <span class="progress-bar">
          <span
            class="progress-bar-cons"
            :style="{ width: progressCons + '%' }"
          ></span>
        </span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "DecisionCard",
  props: {
    topic: String,
    progressPros: Number,
    progressCons: Number,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.decision-card {
  background-color: var(--white);
  box-shadow: 0px 0px 10px -11px;
  border-radius: 10px;
  text-align: left;
  padding: 1em 1em;
  margin: 0.5em 1em;

  .decision-card-content {
    h3 {
      margin: 0;
      padding: 0;
      font-size: 1em;
    }

    .subtitle {
      font-size: 0.8em;
    }

    .decision-progress-bars {
      display: flex;
      flex-direction: row;
      justify-content: space-between;

      .progress-bar {
        width: 48%;
        height: 4px;
        background-color: var(--grey);
        border-radius: 4px;
        position: relative;

        .progress-bar-pros,
        .progress-bar-cons {
          height: 100%;
          position: absolute;
          border-radius: 4px;
        }

        .progress-bar-pros {
          background-color: var(--pros-light);
        }

        .progress-bar-cons {
          background-color: var(--cons-light);
        }
      }
    }
  }
}
</style>
