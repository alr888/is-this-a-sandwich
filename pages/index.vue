<template>
  <main>
    <app-mainbk />
    <app-wut v-if="showWut" />
  </main>
</template>

<script>
import AppMainbk from "~/components/AppMainbk.vue";
import AppWut from "@/components/AppWut.vue";
import { mapState } from "vuex";

export default {
  components: {
    AppWut,
    AppMainbk,
  },
  computed: {
    ...mapState(["showWut"]),
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
