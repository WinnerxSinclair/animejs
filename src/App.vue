<script setup>
import { ref } from 'vue';
import NineBall from './components/NineBall.vue';
import DayNight from './components/DayNight.vue';
import BallImg from './assets/9ball.png'
import SunImg from './assets/sun.png'

const animes = ref([
   { name: '9-ball', logo: BallImg },
   { name: 'Day-to-Night', logo: SunImg}
])

const name = ref('9-ball')
</script>

<template>
  <nav>
    <div class="flex-c-c gap label" v-for="anime in animes" 
    :key="anime.name" 
    @click="name=anime.name" :class="{greybg: anime.name == name }">
      <img :src="anime.logo" alt="" class="logo">
      <div>{{ anime.name }}</div>
    </div>
  </nav>
  <div class="flex-c-c containerxd">
    <NineBall v-if="name=='9-ball'" />
    <DayNight v-if="name=='Day-to-Night'" />
  </div>
</template>

<style scoped>
.containerxd{
  width:80%;
}
nav{
  width: 20%;
}
.greybg{
  background: rgba(143, 143, 143, 0.166);
}
.label{
  border-radius:1rem;
  padding: 1rem 0;
  margin-bottom:.2rem;
  cursor:pointer;
}
.label:hover{
  background: rgba(143, 143, 143, 0.166);
}
.gap{
  gap: 1rem;
}
.flex-c-c{
  display:flex;
  justify-content: center;
  align-items: center;
}
.logo{
  width:30px;
}
</style>