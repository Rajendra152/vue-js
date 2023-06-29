<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button>{{count}}</button>
    <button @click="increment">{{increment}}</button>
    <button @click="doubleCount">{{doubleCount}}</button>
  </div>
</template>

<script setup>
import {useCounterStore} from '../stores/counter';

const { count, doubleCount, increment }= useCounterStore();
console.log(count, doubleCount, increment);


</script>
      
<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
