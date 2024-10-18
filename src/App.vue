<template>
  <div id="app">
    <!-- <BasicUse msg="msg" /> -->
    <!-- {{ msg }} -->
    <!-- <computed /> -->
    <!-- <watch /> -->
    <!-- <classUse /> -->
    <!-- <vIf /> -->
    <!-- <vFor /> -->
    <!-- <event /> -->
    <!-- <index /> -->
    <!-- <indexModel /> -->
    <!-- <nextTick /> -->
    <slotIndex />
    <test />
  </div>
</template>

<script>
import BasicUse from './components/BasicUse.vue';
import computed from './components/computed.vue';
import watch from './components/watch.vue';
import classUse from './components/classUse.vue';
import vIf from './components/v-if.vue';
import vFor from './components/v-for.vue';
import event from './components/event.vue';    //understand
import index from './components/组件通信/index.vue';
import indexModel from './components/自定义v-model/indexModel.vue';
import nextTick from './components/nextTick.vue';
import slotIndex from './components/slot/slotIndex.vue';


import test from './components/test.vue';

export default {
  name: 'App',
  components: {
    BasicUse,
    computed,
    test,
    watch,
    classUse,
    vIf,
    vFor,
    event,
    index,
    indexModel,
    nextTick,
    slotIndex
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
