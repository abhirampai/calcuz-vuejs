<template>
  <div class="calculator">
    <div class="display">{{current || '0'}}</div>
    <div @click="clear" class="btn ac">AC</div>
     <div class="btn ac">+/-</div>
      <div class="btn ac">%</div>
       <div class="btn op">/</div>
        <div class="btn">7</div>
         <div class="btn">8</div>
          <div class="btn">9</div>
           <div class="btn op">x</div>
            <div class="btn">4</div>
             <div class="btn">5</div>
              <div class="btn">6</div>
               <div class="btn op">-</div>
                <div class="btn">1</div>
                 <div class="btn">2</div>
                  <div class="btn">3</div>
                  <div class="btn op">+</div>
                  <div class="btn zero">0</div>
                  <div class="btn">.</div>
                  <div class="btn op">=</div>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data(){
    return{
      current: '123',
    }

  },
  methods:{
    clear(){
      this.current="";
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.calculator
{ 
  margin: 0 auto;
  width:400px;
  font-size:42px;
  display:grid;
  grid-template-columns: repeat(4,1fr);
  grid-template-rows: minmax(50px,auto);
}
.display
{
  grid-column: 1 / 5;
  background-color: blueviolet;

}
.zero
{
  grid-column: 1/3;
}
.btn
{
  background-color:white;
  border:1px solid #999;

}
.op
{
  background-color: black;
  color:white
}
.ac
{
  background-color: orange;
  color:white;

}
</style>
