<template>
	<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
  <table border="2" width="100%" height="100%" id="table">
    <tr>
      <td style="text-align: center" class="nometales">
        <h5 class="num-at" v-on:click="sum(0)">1.00</h5>
        <h3 class="elem">H</h3>
        <h4 class="valence">+1</h4>
      </td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row">  
      <h3 id="masa_molar_total"></h3>
      <button type="button" v-on:click="reset()">Reset</button>
      </td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td style="text-align: center" class="inerte">
        <h5 class="num-at" v-on:click="sum(1)">4.00</h5>
        <h3 class="elem">He</h3>
        <h4 class="valence">0</h4>
      </td>
    </tr>
    <tr>
      <td style="text-align: center" class="alcalino">
        <h5 class="num-at" v-on:click="sum(2)">6.94</h5>
        <h3 class="elem">Li</h3>
        <h4 class="valence">+1</h4>
      </td>        
      <td style="text-align: center" class="alcalinoterreo">
        <h5 class="num-at" v-on:click="sum(3)">9.01</h5>
        <h3 class="elem">Be</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td style="text-align: center" class="metaloides">
        <h5 class="num-at" v-on:click="sum(4)">10.81</h5>
        <h3 class="elem">B</h3>
        <h4 class="valence">±3</h4>
      </td>
      <td style="text-align: center" class="nometales">
        <h5 class="num-at" v-on:click="sum(5)">12.01</h5>
        <h3 class="elem">C</h3>
        <h4 class="valence">+2 ±4</h4>
      </td>
      <td style="text-align: center" class="nometales">
        <h5 class="num-at" v-on:click="sum(6)">14.00</h5>
        <h3 class="elem">N</h3>
        <h4 class="valence">+2 ±3 +4 +5</h4>
      </td>
      <td style="text-align: center" class="nometales">
        <h5 class="num-at" v-on:click="sum(7)">16.00</h5>
        <h3 class="elem">O</h3>
        <h4 class="valence">-2 -1</h4>
      </td>
      <td style="text-align: center" class="halogenos">
        <h5 class="num-at" v-on:click="sum(8)">19.00</h5>
        <h3 class="elem">F</h3>
        <h4 class="valence">-1</h4>
      </td>
      <td style="text-align: center" class="inerte">
        <h5 class="num-at" v-on:click="sum(9)">20.18</h5>
        <h3 class="elem">Ne</h3>
        <h4 class="valence">0</h4>
      </td>
    </tr>
    <tr>
      <td style="text-align: center" class="alcalino">
        <h5 class="num-at" v-on:click="sum(10)">23.00</h5>
        <h3 class="elem">Na</h3>
        <h4 class="valence">+1</h4>
      </td>
      <td style="text-align: center" class="alcalinoterreo">
        <h5 class="num-at" v-on:click="sum(11)">24.30</h5>
        <h3 class="elem">Mg</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td style="text-align: center" class="metales">
        <h5 class="num-at" v-on:click="sum(12)">26.98</h5>
        <h3 class="elem">Al</h3>
        <h4 class="valence">+3</h4>
      </td>
      <td style="text-align: center" class="metaloides">
        <h5 class="num-at" v-on:click="sum(13)">28.08</h5>
        <h3 class="elem">Si</h3>
        <h4 class="valence">+4 -4</h4>
      </td>
      <td style="text-align: center" class="nometales">
        <h5 class="num-at" v-on:click="sum(14)">30.97</h5>
        <h3 class="elem">P</h3>
        <h4 class="valence">+1 +3 +5 -3</h4>
      </td>
      <td style="text-align: center" class="nometales">
        <h5 class="num-at" v-on:click="sum(15)">32.06</h5>
        <h3 class="elem">S</h3>
        <h4 class="valence">±2 +4 +6</h4>
      </td>
      <td style="text-align: center" class="halogenos">
        <h5 class="num-at" v-on:click="sum(16)">35.45</h5>
        <h3 class="elem">Cl</h3>
        <h4 class="valence">±1 +3 +5 +7</h4>
      </td>
      <td style="text-align: center" class="inerte">
        <h5 class="num-at" v-on:click="sum(17)">39.94</h5>
        <h3 class="elem">Ar</h3>
        <h4 class="valence">0</h4>
      </td>
    </tr>
    <tr>
      <td style="text-align: center" class="alcalino">
        <h5 class="num-at" v-on:click="sum(18)">39.10</h5>
        <h3 class="elem">K</h3>
        <h4 class="valence">+1</h4>
      </td>
      <td style="text-align: center" class="alcalinoterreo">
        <h5 class="num-at" v-on:click="sum(19)">40.08</h5>
        <h3 class="elem">Ca</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(20)">44.95</h5>
        <h3 class="elem">Sc</h3>
        <h4 class="valence">+3</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(21)">47.90</h5>
        <h3 class="elem">Ti</h3>
        <h4 class="valence">+3 +4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(22)">50.94</h5>
        <h3 class="elem">V</h3>
        <h4 class="valence">+2 +3 +4 +5</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(23)">52.00</h5>
        <h3 class="elem">Cr</h3>
        <h4 class="valence">+2 +3 +6</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(24)">54.94</h5>
        <h3 class="elem">Mn</h3>
        <h4 class="valence">+2 +3 +4 +6 +7</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(25)">55.84</h5>
        <h3 class="elem">Fe</h3>
        <h4 class="valence">+2 +3</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(26)">58.93</h5>
        <h3 class="elem">Co</h3>
        <h4 class="valence">+2 +3</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(27)">58.69</h5>
        <h3 class="elem">Ni</h3>
        <h4 class="valence">+2 +3</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(28)">63.54</h5>
        <h3 class="elem">Cu</h3>
        <h4 class="valence">+1 +2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(29)">65.39</h5>
        <h3 class="elem">Zn</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td style="text-align: center" class="metales">
        <h5 class="num-at" v-on:click="sum(30)">69.72</h5>
        <h3 class="elem">Ga</h3>
        <h4 class="valence">+3</h4>
      </td>
      <td style="text-align: center" class="metaloides">
        <h5 class="num-at" v-on:click="sum(31)">72.64</h5>
        <h3 class="elem">Ge</h3>
        <h4 class="valence">+4</h4>
      </td>
      <td style="text-align: center" class="metaloides">
        <h5 class="num-at" v-on:click="sum(32)">74.92</h5>
        <h3 class="elem">As</h3>
        <h4 class="valence">+3 +5 -3</h4>
      </td>
      <td style="text-align: center" class="nometales">
        <h5 class="num-at" v-on:click="sum(33)">78.96</h5>
        <h3 class="elem">Se</h3>
        <h4 class="valence">±2 +4 +6</h4>
      </td>
      <td style="text-align: center" class="halogenos">
        <h5 class="num-at" v-on:click="sum(34)">79.90</h5>
        <h3 class="elem">Br</h3>
        <h4 class="valence">±1 +3 +5 +7</h4>
      </td>
      <td style="text-align: center" class="inerte">
        <h5 class="num-at" v-on:click="sum(35)">83.80</h5>
        <h3 class="elem">Kr</h3>
        <h4 class="valence">0</h4>
      </td>
    </tr>
    <tr>
      <td style="text-align: center" class="alcalino">
        <h5 class="num-at" v-on:click="sum(36)">85.47</h5>
        <h3 class="elem">Rb</h3>
        <h4 class="valence">+1</h4>
      </td>
      <td style="text-align: center" class="alcalinoterreo">
        <h5 class="num-at" v-on:click="sum(37)">87.62</h5>
        <h3 class="elem">Sr</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(38)">88.9</h5>
        <h3 class="elem">Y</h3>
        <h4 class="valence">+3</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(39)">91.22</h5>
        <h3 class="elem">Zr</h3>
        <h4 class="valence">+4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(40)">92.9</h5>
        <h3 class="elem">Nb</h3>
        <h4 class="valence">+3 +5</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(41)">95.94</h5>
        <h3 class="elem">Mo</h3>
        <h4 class="valence">+2 +3 +4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(42)">98.9</h5>
        <h3 class="elem">Tc</h3>
        <h4 class="valence">+7</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(43)">101</h5>
        <h3 class="elem">Ru</h3>
        <h4 class="valence">+6 +4 +3 +2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(44)">102.9</h5>
        <h3 class="elem">Rh</h3>
        <h4 class="valence">+2 +3 +4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(45)">106.4</h5>
        <h3 class="elem">Pd</h3>
        <h4 class="valence">+2 +4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(46)">107.9</h5>
        <h3 class="elem">Ag</h3>
        <h4 class="valence">+1</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(47)">122.4</h5>
        <h3 class="elem">Cd</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td style="text-align: center" class="metales">
        <h5 class="num-at" v-on:click="sum(48)">114.8</h5>
        <h3 class="elem">In</h3>
        <h4 class="valence">+3</h4>
      </td>
      <td style="text-align: center" class="metales">
        <h5 class="num-at" v-on:click="sum(49)">118.7</h5>
        <h3 class="elem">Sn</h3>
        <h4 class="valence">+2 +4</h4>
      </td>
      <td style="text-align: center" class="metaloides">
        <h5 class="num-at" v-on:click="sum(50)">121.7</h5>
        <h3 class="elem">Sb</h3>
        <h4 class="valence">+3 +5 -3</h4>
      </td>
      <td style="text-align: center" class="metaloides">
        <h5 class="num-at" v-on:click="sum(51)">127.6</h5>
        <h3 class="elem">Te</h3>
        <h4 class="valence">+4 +6 -2</h4>
      </td>
      <td style="text-align: center" class="halogenos">
        <h5 class="num-at" v-on:click="sum(52)">126.9</h5>
        <h3 class="elem">I</h3>
        <h4 class="valence">±1 +3 +5 +7</h4>
      </td>
      <td style="text-align: center" class="inerte">
        <h5 class="num-at" v-on:click="sum(53)">131.3</h5>
        <h3 class="elem">Xe</h3>
        <h4 class="valence">0</h4>
      </td>
    </tr>
    <tr>
      <td style="text-align: center" class="alcalino">
        <h5 class="num-at" v-on:click="sum(54)">132.9</h5>
        <h3 class="elem">Cs</h3>
        <h4 class="valence">+1</h4>
      </td>
      <td style="text-align: center" class="alcalinoterreo">
        <h5 class="num-at" v-on:click="sum(55)">137.3</h5>
        <h3 class="elem">Ba</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(56)">138.9</h5>
        <h3 class="elem">La</h3>
        <h4 class="valence">+3</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(57)">178.5</h5>
        <h3 class="elem">Hf</h3>
        <h4 class="valence">+4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(58)">180.9</h5>
        <h3 class="elem">Ta</h3>
        <h4 class="valence">+5</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(59)">183.8</h5>
        <h3 class="elem">W</h3>
        <h4 class="valence">+5 +6</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(60)">186.2</h5>
        <h3 class="elem">Re</h3>
        <h4 class="valence">+7 +6 +4 +2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(61)">190.2</h5>
        <h3 class="elem">Os</h3>
        <h4 class="valence">+6 +4 +3 +2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(62)">192.2</h5>
        <h3 class="elem">Ir</h3>
        <h4 class="valence">+2 +3 +4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(63)">195.1</h5>
        <h3 class="elem">Pt</h3>
        <h4 class="valence">+2 +4</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(64)">197</h5>
        <h3 class="elem">Au</h3>
        <h4 class="valence">+1 +3</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(65)">200.6</h5>
        <h3 class="elem">Hg</h3>
        <h4 class="valence">+1 +2</h4>
      </td>
      <td style="text-align: center" class="metales">
        <h5 class="num-at" v-on:click="sum(66)">204.4</h5>
        <h3 class="elem">Tl</h3>
        <h4 class="valence">+1 +3</h4>
      </td>
      <td style="text-align: center" class="metales">
        <h5 class="num-at" v-on:click="sum(67)">207.2</h5>
        <h3 class="elem">Pb</h3>
        <h4 class="valence">+2 +4</h4>
      </td>
      <td style="text-align: center" class="metales">
        <h5 class="num-at" v-on:click="sum(68)">209</h5>
        <h3 class="elem">Bi</h3>
        <h4 class="valence">+3 +5</h4>
      </td>
      <td style="text-align: center" class="metaloides">
        <h5 class="num-at" v-on:click="sum(69)">209</h5>
        <h3 class="elem">Po</h3>
        <h4 class="valence">+2 +4</h4>
      </td>
      <td style="text-align: center" class="halogenos">
        <h5 class="num-at" v-on:click="sum(70)">210</h5>
        <h3 class="elem">At</h3>
        <h4 class="valence">±1 +3 +5 +7</h4>
      </td>
      <td style="text-align: center" class="inerte">
        <h5 class="num-at" v-on:click="sum(71)">222</h5>
        <h3 class="elem">Rn</h3>
        <h4 class="valence">0</h4>
      </td>
    </tr>
    <tr>
      <td style="text-align: center" class="alcalino">
        <h5 class="num-at" v-on:click="sum(72)">223</h5>
        <h3 class="elem">Fr</h3>
        <h4 class="valence">+1</h4>
      </td>
      <td style="text-align: center" class="alcalinoterreo">
        <h5 class="num-at" v-on:click="sum(73)">226</h5>
        <h3 class="elem">Ra</h3>
        <h4 class="valence">+2</h4>
      </td>
      <td style="text-align: center" class="metal-trans">
        <h5 class="num-at" v-on:click="sum(74)">227.0</h5>
        <h3 class="elem">Ac</h3>
        <h4 class="valence">+3</h4>
      </td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
      <td class="no-row"></td>
    </tr>
  </table>
  <div class="overlay" id="overlay">
    <div class="popup" id="popup">

      <a href="#" id="btn-cerrrar-popup" v-on:click="CerrarPopup()" class="btn-cerrar-popup"><i class="fa fa-times"></i></a>
      <h5 style="30px">Numero de atomos</h5>
      <div class="buttons">
        <button class="button">1</button>
        <button class="button">2</button>
        <button class="button">3</button>
        <button class="button">4</button>
        <button class="button">5</button>
        <button class="button">6</button>
        <button class="button">7</button>
        <button class="button">8</button>
        <button class="button">9</button>
        <button class="button">+</button>
      </div>

    </div>
  </div>
</template>

<script>
var vueProp=0;
export default {
  name: 'TableElements',

  methods:{
    sum: function(pos){
      var x=document.getElementById("table").querySelectorAll("h5");
      var value=document.getElementById("table").querySelector
      value=x[pos].innerHTML;
      this.total_var(value);
    },
    /*
    reset:function(){
      if (confirm('Do you really want to reset the count?')) {
        vueProp=0;
        document.getElementById("masa_molar_total").innerHTML=vueProp
      }else {
        console.log("No reseted")
      }
    },*/
    reset:function(){
      vueProp=0;
      document.getElementById("masa_molar_total").innerHTML=vueProp
    },
    total_var: function(num){
      var number= parseFloat(num)
      //console.log(vueProp)
      vueProp=vueProp+number;
      var rounded = Math.round((vueProp + Number.EPSILON) * 100) / 100;
      document.getElementById("masa_molar_total").innerHTML=rounded
    },
    AbrirPopup:function(){
      document.getElementById("overlay").classList.add("active");
      document.getElementById("popup").classList.add("active");

    },
    CerrarPopup:function(){
      document.getElementById("overlay").classList.remove("active");
      document.getElementById("popup").classList.remove("active");

    }
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.contenedor article .btn-abrir-popup {
	padding: 0 20px;
	margin-bottom: 20px;
	height: 40px;
	line-height: 40px;
	border: none;
	color: #fff;
	background: #5E7DE3;
	border-radius: 3px;
	font-family: 'Montserrat', sans-serif;
	font-size: 16px;
	cursor: pointer;
	transition: .3s ease all;
	cursor: pointer;
}
.overlay{
  background-color: rgba(0, 0, 0, .3);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  visibility: hidden;
  
}
.overlay.active{
  visibility: visible;
}
.popup.active{
  opacity: 1;
}
.button{
  padding-top:10px;
  padding-bottom:10px;
  padding-left:10px;
  padding-right:10px;
  font-size: 16px;
  align-items: center;
}
.popup{
  background-color: #f8f8f8;
  box-shadow: 0px 0px 5px 0px rgba(0, 0, 0,.3);
  border-radius: 3px;
  padding:40px;
  text-align: center;
  width: 40%;
  transition: .3s ease all;
  opacity:0;

}
.popup .btn-cerrar-popup{
  font-size:16px;
  line-height: 16px;
  display: block;
  text-align: right;
  color:#BBBBBB;
  transition:.3s ease all;

}
.popup .btn-cerrar-popup:hover{
  color:black;
}
.no-row {
  border:none;
}
.nometales{
  background-color: #A2F0F1;
}
.alcalino{
  background-color: #e78463;
}
.alcalinoterreo{
  background-color: #be9f4f;
}
.inerte{
  background-color:#a97bca;
}
.metal-trans{
  background-color:#95E28C;
}
.metales{
  background-color:#8C8C8C;
}
.metaloides{
  background-color:#6C99E3;
}
.halogenos{
  background-color:#e98dc4;
}
#table h3 {
  font-size: 18px;
}
#table h4{
  font-size: 12px;
}
.popup h5{  font-size: 27px;

}
table{
  table-layout: fixed;
}

</style>
        