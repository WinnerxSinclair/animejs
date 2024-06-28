<script setup>
import { onMounted, onUnmounted } from 'vue';
import anime from 'animejs/lib/anime.es.js';


onMounted(() =>{
  anime({
  targets: '.cloud1',
  keyframes:[
    {translateX: '-500%',  duration: 8000, easing:'linear'},
    {translateX: '20%', duration:1},
    {translateX: '-400%', duration: 8000, easing:'easeOutSine'},
    {translateX: '-700%', duration: 6000, easing:'linear',delay:30000},

    
  ],
   
})
anime({
  targets: '.cloud2',
  keyframes:[
    {translateX: '-700%', duration: 12000, easing:'linear',},
    {translateX: 0, duration:1},
    {translateX: '-400%', duration: 8000, easing:'easeOutSine'},
    {translateX: '-700%', duration: 6000, easing:'linear',delay:26000},

    
  ], 
})
anime({
  targets: '.cloud3',
  keyframes:[
    {translateX: '-300%', duration: 6000, easing:'linear',delay:20000},
    {translateX: '-700%', duration: 6000, easing:'linear',delay:20000},
    
    
  ], 
})
anime({
  targets: '.cloud4',
  keyframes:[
  {translateX: '-300%', duration: 6000, easing:'linear',delay:20000},
  {translateX: '-700%', duration: 6000, easing:'linear',delay:20000},
  
  ], 
})
anime({
  targets: '.cloud5',
  keyframes:[
  {translateX: '-100%', duration: 6000, easing:'linear',delay:20000},
  {translateX: '100%', duration: 6000, easing:'linear',delay:20000},
  
    
  ], 
})
anime({
  targets: '.cloud6',
  keyframes:[
  {translateX: '-100%', duration: 6000, easing:'linear',delay:20000},
  {translateX: '100%', duration: 6000, easing:'linear',delay:20000},
  
    
  ], 
})
let timelineCloud = anime.timeline({
  easing: 'linear',
})
timelineCloud
    .add({
      targets: '.cloud',
      delay: 26000,
      keyframes: [
        { filter: ['brightness(1)', 'brightness(.5)'], duration: 1000, easing: 'linear' },
        { filter: ['brightness(.5)', 'brightness(1)'], duration: 1000,delay: 20000, easing: 'linear' },
      ],
    })
    

anime({
  targets: '.portrait',
  delay: 27000,
  easing: 'linear',
  keyframes: [
    {filter: ['grayscale(100%)'], duration: 1000,},
    {filter: ['grayscale(0%)'], duration: 1000,delay: 20000},
    {backgroundColor: '#000', duration: 60000},
    
    
  ] 
})

anime({
  targets: '.sun',
  delay: 49000,
  keyframes: [
    {translateY: '400%', duration: 25000, easing: 'linear'}
  ]
})
anime({
  targets: '.moon',
  delay: 60000,
  keyframes: [
    {translateY: '-400%', duration: 30000, easing: 'linear'}
  ]
})


setTimeout(() => {
  anime({
    targets: '.rain',
    translateY: ['-100%', '10000%'],
    easing: 'linear',
    loop: 2,
    duration: function() { return Math.random() * 500; },
    delay: anime.stagger(16)
  });
}, 28000); 

    anime({
      targets: '.star',
      opacity: 1,
      duration: 15000,
      delay: 70000,
      easing: 'linear',
    });
    setTimeout(() => {
    anime({
      targets: '.star',
      keyframes: [
        { filter: ['brightness(40%)', 'brightness(100%)'], scale: '1.3' },
        { filter: ['brightness(100%)', 'brightness(40%)'], scale: '1' },
      ],
      duration: function() { return Math.random() * 5000; },
      delay: anime.stagger(500),
      easing: 'linear',
      loop: 3,
    });
  }, 85000);
  anime({
    targets: '.hill',
    filter: ['brightness(100%)', 'brightness(40%)'],
    duration:60000,
    delay:47000,
    easing: 'linear'
  })
})
</script>

<template>
  <div class="portrait">
    <div v-for="n in 480" :key="n" class="rain" :style="{ left: `${Math.random() * 100}%` }"></div>
    <div v-for="n in 50" :key="n" class="star" :style="{ left: `${Math.random() * 100}%`, top: `${Math.random() * 30}vh`  }"></div>
    <div class="sun"></div>
    <div class="moon"></div>
    <img src="../assets/cloud.png" alt="" class="cloud cloud1">
    <img src="../assets/cloud.png" alt="" class="cloud cloud2">
    <img src="../assets/cloud.png" alt="" class="cloud cloud3">
    <img src="../assets/cloud.png" alt="" class="cloud cloud4">
    <img src="../assets/cloud.png" alt="" class="cloud cloud5">
    <img src="../assets/cloud.png" alt="" class="cloud cloud6">
    <div class="airplane"></div>
    <div class="hill">
      <div class="power-lines pl1"></div>
      <div class="power-lines pl2"></div>
      <div class="power-lines pl3"></div>
      <div class="power-lines pl4"></div>
      <div class="power-lines pl5"></div>
      <div class="power-lines pl6"></div>
      <div class="house">
        <div class="chimney"></div>
        <div class="roof">
          
        </div>
        <div class="body">
          <div class="door">
            <div class="knob"></div>
          </div>
          <div class="window">
            <div class="pane"></div>
            <div class="pane"></div>
            <div class="pane"></div>
            <div class="pane"></div>
          </div>
        </div>
      </div>
    </div>
   
  </div>
</template>

<style scoped>
*{
  box-sizing:border-box;
}
.star{
  position:absolute;
  background:white;
  width:10px;
  aspect-ratio: 1;
  clip-path: polygon(49% 6%, 59% 37%, 90% 37%, 66% 57%, 79% 87%, 49% 69%, 18% 88%, 31% 54%, 8% 37%, 37% 36%);
  opacity:0;
  filter: brightness(40%);
  
}
.moon{
  position:absolute;
  bottom:5%;
  right:10%;
  
    width: 100px;
    height: 100px;
    background-color: transparent;
    border-radius: 50%;
    box-shadow: 25px 10px 0px 0px yellow;
}

.cloud{
  position:absolute;
  width:100%;
  right:-70%;
}
.cloud1{
  scale: .25;
  top:-20%;
}
.cloud2{
  scale: .2;
  top:-30%;
}
.cloud3{
  top: -40%;
  scale:.3;
}
.cloud4{
  top: -20%;
  scale:.4;
}
.cloud5{
  top: -25%;
  scale:.5;
}
.cloud6{
  top: -40%;
  scale: .3;
}
.portrait{
  position:relative;
  background: rgb(98, 210, 255);
 
  height:600px;
  width:100%;
  max-width:1200px;
  display:flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  overflow:hidden;
  
}
.rain{
  position:absolute;
  height:40px;
  width:2px;
  background:rgb(255, 255, 255);
  top:-10%;
  rotate:-4deg;
  z-index: 2;
}

.hill{
  width:120%;
  height:50%;
  border-radius: 50% 50% 0 0;
  background:green;
  position:relative;
  z-index:1;
}
.house{
  position:absolute;
  right:20%;
  top:0;
  width:15%;
  height:50%;
  z-index:2;
}
.roof{
  width:100%;
  height:40%;
  clip-path:polygon(50% 0, 0 100%, 100% 100%);
  background:brown;
  position:relative;
  
}
.chimney{
  position:absolute;
  right:15%;
  top:15%;
  height:15%;
  width:10%;
  background:black;
  z-index:55;
}
.body{
  height:60%;
  background: linear-gradient(to top, rgb(221, 81, 81) 20%, brown 20% 40%,
   rgb(221, 81, 81) 40% 60%,  brown 60% 80%,  rgb(221, 81, 81) 80% );
  width:100%;
  position:relative;
}
.door{
  position:absolute;
  width:20%;
  height:50%;
  background:rgb(62, 36, 36);
  left:50%;
  top:50%;
  transform: translate(-50%, 0%);
}
.knob{
  position:absolute;
  right: 10%;
  top:50%;
  width:20%;
  aspect-ratio: 1;
  border-radius: 50%;
  background:yellow;
}
.window{
  width:15%;
  aspect-ratio: 1;
  position:absolute;
  display:flex;
  flex-wrap: wrap;
  left:10%;
  top:10%;
  background:rgb(0, 217, 255);
  border: 1px solid black;
}
.pane{
  width:50%;
  height:50%;
  border:1px solid black;
}
.sun{
  position:absolute;
  top: 5%;
  right: 10%;
  width: 100px;
    height: 100px;
  background:yellow;
  border-radius: 50%;
}
</style>