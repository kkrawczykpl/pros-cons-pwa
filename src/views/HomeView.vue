<template>
  <div class="home">
    <nav>
      <ul>
        <li>
          <router-link to="/"
            ><img src="../assets/images/card-add.svg" alt="Add new topic"
          /></router-link>
        </li>
      </ul>
    </nav>
    <header>
      <h1>My decisions</h1>
    </header>
    <main>
      <div class="decisions-list">
        <DecisionCard
          topic="Buy a new bike"
          progressPros="43"
          progressCons="57"
        ></DecisionCard>
        <DecisionCard
          topic="Buy RTX 3080"
          progressPros="70"
          progressCons="30"
        ></DecisionCard>
        <DecisionCard
          topic="Go back to College"
          progressPros="15"
          progressCons="85"
        ></DecisionCard>
        <router-link to="/"><AddCard></AddCard></router-link>
      </div>
    </main>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import DecisionCard from "@/components/DecisionCard.vue";
import AddCard from "@/components/AddCard.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    DecisionCard,
    AddCard,
  },
});
</script>

<style lang="scss" scoped>
.home {
  width: 100%;

  nav {
    ul {
      list-style: none;

      li {
        width: 100%;
        height: 100%;

        a {
          img {
            float: right;
            margin-right: 1em;
            width: 1.5em;
            color: var(--white);
          }
        }
      }
    }
  }
}

.decisions-list {
  display: flex;
  justify-content: center;
  flex-direction: column;
}

header > h1 {
  text-align: left;
  margin: 0;
  padding: 0;
  margin-left: 0.5em;
  font-size: 1.5em;
}

a {
  text-decoration: none;
}
</style>
