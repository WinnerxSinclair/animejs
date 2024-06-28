<script setup>
import { onMounted, onUnmounted } from 'vue';
import anime from 'animejs/lib/anime.es.js';

let timelineStick, timelineCue, timelineOne, timelineTwo, timelineThree, timelineFour, timelineFive, timelineSix, timelineSeven, timelineEight, timelineNine;

onMounted(() => {
   timelineStick = anime.timeline({
    easing: 'linear'
  });
   timelineCue = anime.timeline({
    easing: 'linear'
  });
   timelineOne = anime.timeline({
    easing: 'linear'
  });
   timelineTwo = anime.timeline({
    easing: 'linear'
  });
   timelineThree = anime.timeline({
    easing: 'linear'
  });
   timelineFour = anime.timeline({
    easing: 'linear'
  });
   timelineFive = anime.timeline({
    easing: 'linear'
  });
   timelineSix = anime.timeline({
    easing: 'linear'
  });
   timelineSeven = anime.timeline({
    easing: 'linear'
  });
   timelineEight = anime.timeline({
    easing: 'linear'
  });
   timelineNine = anime.timeline({
    easing: 'linear'
  });
  timelineStick
    .add({
      targets: '.stick',
     
      translateX: [
        { value: '20%', duration: 1000 },
        { value: '-5%', duration: 100 }
      ],
      easing: 'linear'
    })
    .add({
      targets: '.stick',
      keyframes: [
        {opacity: 0,delay: 200},
        {translateX: -290, rotate: '-150deg', translateY: 320},
        {opacity:1, delay: 3000}
      ]
    })
    .add({
      targets: '.stick',
      keyframes: [
        {translateX: -330, translateY: 400, duration: 1100},
        {translateX: -285, translateY: 310, duration: 100}
      ] 
    })
    .add({
      targets: '.stick',
      keyframes: [
        {opacity: 0,delay: 200},
        {translateX: -40, rotate: '15deg', translateY: 110},
        {opacity:1, delay: 2800}
      ]
    })
    .add({
      targets: '.stick',
      keyframes: [
        {translateX: -10, translateY: 140, duration: 1100},
        {translateX: -45, translateY: 108,  duration: 100}
      ] 
    })
    .add({
      targets: '.stick',
      keyframes: [
        {opacity: 0,delay: 200},
        {translateX: -90, rotate: '-30deg', translateY: -160},
        {opacity:1, delay: 2800}
      ]
    })
    .add({
      targets: '.stick',
      keyframes: [
        {translateX: -70, translateY: -200, duration: 1100},
        {translateX: -97, translateY: -150,  duration: 100}
      ] 
    })
    .add({
      targets: '.stick',
      keyframes: [
        {opacity: 0,delay: 200},
        {translateX: -92, rotate: '-45deg', translateY: -300},
        {opacity:1, delay: 2800}
      ]
    })
    .add({
      targets: '.stick',
      keyframes: [
        {translateX: -50, translateY: -400, duration: 1100},
        {translateX: -100, translateY: -280,  duration: 100}
      ] 
    })
    .add({
      targets: '.stick',
      keyframes: [
        {opacity: 0,delay: 200},
        {translateX: -275, rotate: '-165deg', translateY: -38},
        {opacity:1, delay: 2800}
      ]
    })
    .add({
      targets: '.stick',
      keyframes: [
        {translateX: -300, translateY: -15, duration: 1100},
        {translateX: -272, translateY: -40,  duration: 100}
      ] 
    })
    .add({
      targets: '.stick',
      keyframes: [
        {opacity: 0,delay: 200},
        {translateX: -1, rotate: '65deg', translateY:671},
        {opacity:1, delay: 2800}
      ]
    })
    .add({
      targets: '.stick',
      keyframes: [
        {translateX:90, translateY: 1000, duration: 1100},
        {translateX: -16, translateY: 610,  duration: 200},
        {opacity: 0, delay:200}
      ] 
    })
    
    
  timelineCue
    .add({
      targets: '.cue',
      translateX: -390,
      translateY: 130,
      duration: 300,
      delay: 1100,
      
    })
    .add({
      targets: '.cue',
      keyframes: [
        { translateX: -500, translateY: 350, duration: 500 },
        { translateX: -663, translateY: 130, duration: 1000 },
        { translateX: -600, translateY: 0, duration: 2000, easing: 'easeOutSine' },
      ], 
    })
    .add({
      targets: '.cue',
      delay: 1600,
      keyframes: [
        { translateX: -50, translateY: 130, duration: 500 },
        { translateX: 95, translateY: -10, duration: 300 },
        { translateX: -20, translateY: -110, duration: 300 },
        { translateX: -180, translateY: 100, duration: 2000, easing: 'easeOutSine' },  
      ], 
    })
    .add({
      targets: '.cue',
      delay: 2100,
      translateX: -420,
      translateY: 100,
      duration: 200,
    })
    .add({
      targets: '.cue',
      delay: 5000,
      keyframes: [
        { translateX: -480, translateY: 150, duration: 50 },
        { translateX: -520, translateY: 100, duration: 2000, easing: 'easeOutSine'}
      ],
    })
    .add({
      targets: '.cue',
      delay: 3100,
      keyframes: [
        { translateX: -580, translateY: 200, duration: 100 },
        { translateX: -615, translateY: 270, duration: 3000, easing: 'easeOutSine'}
      ],
    })
    .add({
      targets: '.cue',
      delay: 2200,
      keyframes: [
        { translateX: -530, duration: 100 },
        { translateX: -450, translateY: 200, duration: 3000, easing: 'easeOutSine'}
      ],
    })
    .add({
      targets: '.cue',
      delay: 2150,
      keyframes: [
        { translateX: -600, translateY: -10, duration: 1000 }
      ],
    })
    

  timelineOne
    .add({
      targets: '.one',
      keyframes: [
        { translateX: 260, translateY: 235, duration: 1000, delay: 1400},
        { translateX: 400, translateY: 50, duration: 2000, easing: 'easeOutSine'}
      ],
    })
    .add({
      targets: '.one',
      translateX: 535,
      translateY: 260,
      delay: 2600,
      duration: 500
    })
    .add({
      targets: '.one',
      opacity: 0,
      duration:1,
      delay: 200,
    })
  timelineTwo
    .add({
      targets: '.two',
      delay: 11900,
      keyframes: [
        { translateX: -200, translateY: -50, duration: 300 },
        { translateX: 570, translateY: -225, duration: 2500, easing: 'easeOutSine'},
        { opacity: 0, delay: 200}
      ]
    }) 
  timelineThree
    .add({
      targets: '.three',
      translateX: -50, 
      translateY: 50, 
      duration: 2000, 
      delay: 1400, 
      easing: 'easeOutSine'
    })
    .add({
      targets: '.three',
      delay: 13500,
      keyframes: [
        { translateX: -140, translateY: 218, duration: 300 },
        { translateX: -205, translateY: 50, duration: 300 },
        { translateX: -205, translateY: 50, duration: 300 },
        { translateX: 175, translateY: -265, duration: 1000, easing: 'easeOutSine' },
        { opacity: 0, duration: 200 }
       
      ]
    })
  
  timelineFive
    .add({
      targets: '.five',
      keyframes: [
        { translateX: -140, translateY: 200, duration: 1000, delay: 1400,},
        { translateX: -168, translateY: 150, duration: 500 },
        { translateX: -100, translateY: 80, duration: 2000, easing: 'easeOutSine' },
      
      ],
    })
    .add({
      targets: '.five',
      delay: 17300,
      keyframes: [
        
        { translateX: -185, translateY: 220, duration: 300 },
        { opacity: 0, delay: 200}
      
      ],
    })
  timelineFour
    .add({
      targets: '.four',
      keyframes: [
        { translateX: -100, translateY: -180, duration: 300, delay: 1400,},
        { translateX: -168, translateY: -100, duration: 150 },
        { translateX: 150, translateY: 278, duration: 800 },
        { translateX: 605, translateY: -205, duration: 2000, easing: 'easeOutSine' },
        { opacity: 0, delay: 200 }
      ],
    })

  timelineSeven
    .add({
        targets: '.seven',
        translateX: -145, translateY: 235, duration: 500, delay: 1400,
      })
    .add({
      targets: '.seven',
      opacity: 0,
      duration:1,
      delay: 200,
    })

  timelineEight
    .add({
      targets: '.eight',
      keyframes: [
        { translateX: -100, translateY: 100, duration: 500, delay: 1400},
        { translateX: 0, translateY: 237, duration: 1000},
        { translateX: 60, translateY: 165, duration: 1500, easing: 'easeOutSine'},
      
      ],
    })
    .add({
      targets: '.eight',
      delay:23000,
      keyframes: [
        { translateX: 680, translateY: 255, duration: 2000},
        { opacity: 0, delay: 200}
      ],
    })
  timelineSix
    .add({
      targets: '.six',
      keyframes: [
        { translateX: -120, translateY: -120, duration: 500, delay: 1400},
        { translateX: -90, translateY: -160, duration: 500},
        { translateX: -147, translateY: -225, duration: 800},
        { opacity: 0, delay: 200}
        
      ],
    })

  timelineNine
  .add({
    targets: '.nine',
    keyframes: [
      { translateX: -120, translateY: -150, duration: 1000, delay: 1400},
      { translateX: -185, translateY: -243, duration: 2000, easing: 'easeOutSine', delay: 31150},
      { opacity: 0, delay: 200 }
    ],
  })
    
});
onUnmounted(() => {
  
  timelineStick.pause();
  timelineCue.pause();
  timelineOne.pause();
  timelineTwo.pause();
  timelineThree.pause();
  timelineFour.pause();
  timelineFive.pause();
  timelineSix.pause();
  timelineSeven.pause();
  timelineEight.pause();
  timelineNine.pause();

  timelineStick.seek(0);
  timelineCue.seek(0);
  timelineOne.seek(0);
  timelineTwo.seek(0);
  timelineThree.seek(0);
  timelineFour.seek(0);
  timelineFive.seek(0);
  timelineSix.seek(0);
  timelineSeven.seek(0);
  timelineEight.seek(0);
  timelineNine.seek(0);
  

});
</script>

<template>
  <div class="table">
    <div class="container">
      <div class="stick"></div>
      <div class="hole-container">
        <div class="hole"></div>
        <div class="hole"></div>
        <div class="hole"></div>
      </div>
      <div class="hole-container">
        <div class="hole"></div>
        <div class="hole"></div>
        <div class="hole"></div>
      </div>
      <div class="ball cue"></div>
      <div class="ball one">1</div>
      <div class="ball two">2</div>
      <div class="ball three">3</div>
      <div class="ball four">4</div>
      <div class="ball five">5</div>
      <div class="ball six">6</div>
      <div class="ball seven">7</div>
      <div class="ball eight">8</div>
      <div class="ball nine">9</div>
    </div>
  </div>
  
</template>

<style scoped>
.stick{
  width:400px;
  height:15px;
  background:black;
  clip-path: polygon(0% 20%, 100% 0%, 100% 100%, 0% 80%);
  border-radius:1rem;
  position:absolute;
  rotate:-15deg;
  right:-300px;
  top:100px;
  overflow:hidden;
  z-index:99;
  
  
}

.table{
  display:flex;
  align-items: center;
  height:500px;
  width:800px;
  background:green;
  border-radius:1rem;
  border: 50px solid brown;
  
}
.container{
  display:flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  height:110%;
  width:100%;
  position:relative;
}
.hole-container{
  display:flex;
  justify-content: space-between;
  width:105%;
  
}
.hole{
  background:black;
  width:50px;
  aspect-ratio: 1;
  border-radius: 50%;
}
.ball{
  position:absolute;
  width:40px;
  aspect-ratio: 1;
  border-radius: 50%;
  color:white;
  opacity:1;
}
.cue{
  background:white;
  right:12%;
  top:25%;
}
.one{
  background:yellow;
  top:45%;
  left:30%;
}
.two{
  background:blue;
  top:41.5%;
  left:25.4%;
}
.three{
  background:red;
  bottom:43.8%;
  left:25.5%;
}
.four{
  top:38%;
  left:21%;
  background: purple;
}
.nine{
  background: lime;
  top:45%;
  left:21%;
}
.five{
  background:orange;
  left:21%;
  top:52%;
}
.six{
  top:41.5%;
  left:16.5%;
  background:rgb(51, 209, 51);
}
.seven{
  background:brown;
  left:16.5%;
  bottom:43.8%;
}
.eight{
  background:black;
  top:45%;
  left:12.2%;
}

</style>
