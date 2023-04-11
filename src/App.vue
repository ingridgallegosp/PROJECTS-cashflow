<template>
    <SplashScreen/>
</template>

<script>
    import SplashScreen from './components/SplashScreen.vue'

    export default {
        components: {
            SplashScreen
        }
    }
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
}
</style>

