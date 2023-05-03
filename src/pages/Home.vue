<template>
    <Layout>
        <template #header>
            <Header></Header>
        </template>
        <template #resume>
            <Resume
            :label-selected="'Date'"
            :general-label="'Ahorro Total'"
            :amount="1000"
            :total-amount="100000">
            </Resume>
        </template>
        <template #movements>
            <Movements></Movements>
        </template> 
  </Layout>
</template>

<script setup>
import Layout from "../components/Layout.vue";
import Header from "../components/Header.vue";
import Resume from "../components/Resume/Index.vue";
import Movements from "../components/Movements.vue";



</script>

<style>
</style>
