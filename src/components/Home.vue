<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume 
        :label="'Total Saved'"
        :total-amount="100000"
        :amount="1000">
        <template #graphic>
          graphic
        </template>
        <template #action>
          action
        </template>
      </Resume>
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
