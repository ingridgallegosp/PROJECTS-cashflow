<template>
  <Suspense>
    <template #default>
      <Home />
    </template>
    <template #fallback>
      <SplashScreen />
    </template>
  </Suspense>
</template>

<script>
//import Home from './components/Home.vue'
import SplashScreen from "./pages/SplashScreen.vue";
import { defineAsyncComponent } from "vue";

export default {
  components: {
    SplashScreen,
    Home: defineAsyncComponent(() => {
      return new Promise((resolve) => {
        setTimeout(() => {
          resolve(import("./pages/Home.vue"));
        }, 2000);
      });
    }),
  },
};
</script>

<style>
html,
body,
.app {
  min-height: 100vh;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
* {
  --brand-green: #04b500;
  --brand-blue: #0689b0;
  --white: #e5e5e5;
}
</style>
