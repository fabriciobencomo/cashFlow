<template>
  <Suspense>
    <template #default>
        <Home></Home>
    </template>
    <template #fallback>
      <Splashscreen></Splashscreen>
    </template>
  </Suspense>
</template>

<script>
import Splashscreen from "@/components/SplashScreen";
import { defineAsyncComponent } from "vue";

export default {
  components: {
    Splashscreen,
    Home: defineAsyncComponent(() => new Promise((resolve) => {
      setTimeout(() => {
        resolve(import("@/components/Home.vue"))
      }, 2000);
    })
    )
  },
};
</script>

<style>
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
