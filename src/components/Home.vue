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
          <Graphic />
        </template>
        <template #action>
          <Action></Action>
        </template>
      </Resume>
    </template>
    <template #movements>
      <Movements 
        :movements="movements" 
      />
    </template>
  </Layout>
</template>

<script>
import Action from "@/components/Action";
import Header from "@/components/Header";
import Layout from "@/components/Layout";
import Movements from "@/components/Movements/Index";
import Resume from "@/components/Resume/Index";
import Graphic from "./Resume/Graphic.vue";

export default {
  components:{
    Header,
    Layout,
    Resume,
    Movements,
    Action,
    Graphic
},
  data(){
    return{
      movements:[
        {
          id:0,
          title:"Movement 1",
          description: "Wage Deposit",
          amount: 1000
        },
        {
          id:1,
          title:"Movement 2",
          description: "Friend Debt",
          amount: 100
        },        
        {
          id:2,
          title:"Movement 3",
          description: "water",
          amount: -70
        },        
        {
          id:3,
          title:"Movement 4",
          description: "Light",
          amount: -100
        },
      ]
    }
  }
};
</script>

<style></style>
