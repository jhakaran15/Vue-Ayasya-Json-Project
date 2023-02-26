<template>
  <q-layout view="lHh Lpr lFf" id="lay-out"> <router-view /></q-layout>
</template>

<script>
import Loading from "vue-loading-overlay";
import "vue-loading-overlay/dist/vue-loading.css";
import { mapState } from "vuex";

export default {
  components: {
    Loading,
  },
  computed: {
    ...mapState({
      isLoading: "isLoading",
    }),
  },
  data() {
    return {
      leftDrawerOpen: false,
      fullPage: true,
    };
  },
};
</script>

<style></style>
