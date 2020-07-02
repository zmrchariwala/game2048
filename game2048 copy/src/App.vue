<template>
  <div id="app">
    <game2048 v-bind:squares="squares" v-on:right-move="rightmove()" v-on:left-move="leftmove()" v-on:up-move="upmove()" v-on:down-move="downmove()"/>
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
  </div>
</template>

<script>

import game2048 from './components/game2048'

export default {
  name: 'App',
  components: {
    game2048
  },
  data(){
    return {
      squares:[
        {
          id:1,
          value:1
        },
        {
          id:2,
          value:1
        },
          {
          id:3
        },
        {
          id:4
        },
          {
          id:5
        },
        {
          id:6
        },
          {
          id:7
        },
        {
          id:8
        },
          {
          id:9
        },
        {
          id:10
        },
          {
          id:11
        },
        {
          id:12
        },
          {
          id:13
        },
        {
          id:14
        },
          {
          id:15
        },
        {
          id:16
        }
      ]
    }
  },
  methods:{
    rightmove(){
      alert("Right");
      if(this.squares[0].value === this.squares[1].value)
      {
        this.squares[1].value = this.squares[0].value + this.squares[1].value;
      }
      alert(this.squares[1].value);
      
    },
    leftmove(){
      alert("Left");
      if(this.squares[0].value === this.squares[1].value)
      {
        this.squares[0].value = this.squares[0].value + this.squares[1].value;
      }
      alert(this.squares[1].value);
      
    },
    upmove(){
      alert("Up");
      if(this.squares[0].value === this.squares[1].value)
      {
        this.squares[0].value = this.squares[0].value + this.squares[1].value;
      }
      alert(this.squares[1].value);
      
    },
    downmove(){
      alert("Down");
      if(this.squares[0].value === this.squares[1].value)
      {
        this.squares[0].value = this.squares[0].value + this.squares[1].value;
      }
      alert(this.squares[1].value);
      
    }
  }
}
</script>


