<template>
  <div class="main-container">
      <h1><span>Game</span> <span>2</span><span>0</span><span>4</span><span>8</span></h1>
      <div class="game-area">
          <div class="game-square" v-bind:key="square.id" v-for="(square) in squares">{{ square.value }}</div>
          
      </div>
      <button v-on:click="$emit('right-move')">Right</button>
      <button v-on:click="$emit('left-move')">Left</button>
      <button v-on:click="$emit('up-move')">Up</button>
      <button v-on:click="$emit('down-move')">Down</button>
  </div>
</template>

<script>

export default {
  name: 'game2048',
  props: ["squares"]
}

</script>

<style scoped>
    h1{
        text-align: center;
    }
    h1 span:nth-child(1){
        color:rgb(150, 81, 22);
    }
    h1 span:nth-child(2){
        color: green;
    }
    h1 span:nth-child(3){
        color:turquoise;
    }
    h1 span:nth-child(4){
        color:orangered;
    }
    h1 span:nth-child(5){
        color:orange;
    }
    .main-container{
        text-align: -webkit-center;
        
    }
    .game-area{
        text-align: center;
        position: relative;
        width: 500px;
        height: 500px;
        background-color:blue;
        display: flex;
        flex-wrap: wrap;
        border-radius: 10px;
    }
    .game-square{
        width: 21%;
        height: 21%;
        margin: 10px;
        border-radius: 10px;;
        background-color: chocolate;
        box-sizing: border-box;
        justify-content: center;
        font-size: 6em;
        font-weight: bold;
        color: white;
    }
</style>