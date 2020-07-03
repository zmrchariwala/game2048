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
          id:3,
          value:""

        },
        {
          id:4,
          value:""
        },
          {
          id:5,
          value:""
        },
        {
          id:6,
          value:""
        },
          {
          id:7,
          value:1
        },
        {
          id:8,
          value:1
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
      if((this.squares[0].value === this.squares[1].value) && ((this.squares[2].value === this.squares[3].value)) && (this.squares[2].value != "" && this.squares[3].value != "" ))
      {
        alert("second");
        this.squares[3].value = this.squares[2].value + this.squares[3].value;
        this.squares[2].value = "";
        this.squares[2].value = this.squares[0].value + this.squares[1].value;
        this.squares[0].value = "";
        this.squares[1].value = "";

      }
      else if((this.squares[0].value == this.squares[1].value) && (this.squares[2].value == "" && this.squares[3].value==""))
      {
        alert("first");
        this.squares[3].value = this.squares[0].value + this.squares[1].value;
        
        this.squares[1].value = "";
        this.squares[0].value ="";
      }
      else if((this.squares[0].value == this.squares[1].value) && (this.squares[2].value == "" && this.squares[3].value!=""))
      {
        alert("first1");
        this.squares[2].value = this.squares[0].value + this.squares[1].value;
        
        this.squares[1].value = "";
        this.squares[0].value ="";
      }
      else if((this.squares[1].value == this.squares[2].value))
      {
        if(this.squares[3].value == "")
        {
          this.squares[3].value = this.squares[1].value + this.squares[2].value;
          if(this.squares[0].value != "")
          {
            this.squares[2].value = this.squares[0].value;
            this.squares[0].value = "";
            this.squares[1].value = "";
          }
        }
        else
        {
          this.squares[2].value = this.squares[1].value + this.squares[2].value;
          this.squares[1].value = this.squares[0].value;
          this.squares[0].value = "";
        }
      }
      else if((this.squares[0].value == this.squares[1].value) && ((this.squares[2].value != "" && this.squares[3].value!="")&& this.squares[2].value != this.squares[3].value))
      {
        alert("first1");
        this.squares[1].value = this.squares[0].value + this.squares[1].value;
        
        //this.squares[1].value = "";
        this.squares[0].value ="";
      }
      else if((this.squares[2].value === this.squares[3].value) && ((this.squares[0].value != this.squares[1].value) && this.squares[0].value !="" && this.squares[1].value != ""))
      {
        alert("2 1 1 1");
        this.squares[3].value = this.squares[2].value + this.squares[3].value;
        this.squares[2].value = this.squares[1].value;
        this.squares[1].value = this.squares[0].value;
        this.squares[0].value ="";
      }
      

      //Second Line

      if((this.squares[4].value === this.squares[5].value) && ((this.squares[6].value === this.squares[7].value)) && (this.squares[6].value != "" && this.squares[7].value != "" ))
      {
        alert("second");
        this.squares[7].value = this.squares[6].value + this.squares[7].value;
        this.squares[6].value = "";
        this.squares[6].value = this.squares[4].value + this.squares[5].value;
        this.squares[4].value = "";
        this.squares[5].value = "";

      }
      else if((this.squares[4].value == this.squares[5].value) && (this.squares[6].value == "" && this.squares[7].value==""))
      {
        alert("first");
        this.squares[7].value = this.squares[4].value + this.squares[5].value;
        
        this.squares[5].value = "";
        this.squares[4].value ="";
      }
      else if((this.squares[4].value == this.squares[5].value) && (this.squares[6].value == "" && this.squares[7].value!=""))
      {
        alert("first1");
        this.squares[6].value = this.squares[4].value + this.squares[5].value;
        
        this.squares[5].value = "";
        this.squares[4].value ="";
      }
      else if((this.squares[5].value == this.squares[6].value))
      {
        if(this.squares[7].value == "")
        {
          this.squares[7].value = this.squares[5].value + this.squares[6].value;
          if(this.squares[4].value != "")
          {
            this.squares[6].value = this.squares[4].value;
            this.squares[4].value = "";
            this.squares[5].value = "";
          }
        }
        else
        {
          this.squares[6].value = this.squares[5].value + this.squares[6].value;
          this.squares[5].value = this.squares[4].value;
          this.squares[4].value = "";
        }
      }
      else if((this.squares[4].value == this.squares[5].value) && ((this.squares[6].value != "" && this.squares[7].value!="")&& this.squares[6].value != this.squares[7].value))
      {
        alert("first1");
        this.squares[5].value = this.squares[4].value + this.squares[5].value;
        
        //this.squares[1].value = "";
        this.squares[4].value ="";
      }
      else if((this.squares[6].value === this.squares[7].value) && ((this.squares[4].value != this.squares[5].value) && this.squares[4].value !="" && this.squares[5].value != ""))
      {
        alert("2 1 1 1");
        this.squares[7].value = this.squares[6].value + this.squares[7].value;
        this.squares[6].value = this.squares[5].value;
        this.squares[5].value = this.squares[4].value;
        this.squares[4].value ="";
      }
      

      
      
      
      //alert(this.squares[1].value);
      
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


