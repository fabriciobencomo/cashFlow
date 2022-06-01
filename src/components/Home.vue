<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume></Resume>
    </template>
    <template #movements>
      <Movements/>
    </template>
  </Layout>
</template>

<script>
import Header from "@/components/Header";
import Layout from "@/components/Layout";
import Movements from "@/components/Movements";
import Resume from "@/components/Resume/Index";

export default {
  components:{
    Header,
    Layout,
    Resume,
    Movements
  }
};
</script>

<style></style>
