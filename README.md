# Working-calculator
<html>
  <head>	
	<title>Calculator</title>
  </head>

    <body>
	  <h1 style="font-size:250%;"><ins> Calculator </ins></h1>
     </body>
  <style>
   table, th, td {
  	border: 3px solid black;
 	 border-style: solid;
}
th {
	text-align: centre;
 	padding: 45px;
}
td {
  	padding: 7px;
}

.text{
  color:red;
}


button {
    padding: 18px;
    font-size: 18px;
    cursor: pointer;
    border-radius: 13px 13px 13px 13px;
}

    </style>

 <body>
      <div class="calculator">
        
        <div class="keys">
  <table>
      <tr>
         <th colspan="4"><input type="text" id="display" readonly></th>
         </tr>
      <tr>
         <td> <button onclick="clearDisplay()"><b> C </b></button> </td>
         <td> <button onclick="appendToDisplay('x')" class="text"> x </button> </td>
	 <td> <button onclick="appendToDisplay('%')" class="text"> % </button> </td>
	 <td> <button onclick="appendToDisplay('/')" class="text"> / </button> </td>
      </tr>

      <tr>
         <td> <button onclick="appendToDisplay('7')"> 7 </button> </td>
         <td> <button onclick="appendToDisplay('8')"> 8 </button> </td>
	 <td> <button onclick="appendToDisplay('9')"> 9 </button> </td>
	 <td> <button onclick="appendToDisplay('*')" class="text"> * </button> </td>
      </tr>

      <tr>
         <td> <button onclick="appendToDisplay('4')"> 4 </button> </td>
         <td> <button onclick="appendToDisplay('5')"> 5 </button> </td>
	 <td> <button onclick="appendToDisplay('6')"> 6 </button> </td>
	 <td> <button onclick="appendToDisplay('-')" class="text"> - </button> </td>
      </tr>

      <tr>
         <td> <button onclick="appendToDisplay('1')"> 1 </button> </td>
         <td> <button onclick="appendToDisplay('2')"> 2 </button> </td>
	 <td> <button onclick="appendToDisplay('3')"> 3 </button> </td>
	 <td> <button onclick="appendToDisplay('+')" class="text"> + </button> </td>
      </tr>

      <tr>
         <td> <button onclick="appendToDisplay('^')" class="text"> ^ </button> </td>
         <td> <button onclick="appendToDisplay('0')"> 0 </button> </td>
	 <td> <button onclick="appendToDisplay('.')" class="text"><b> . </b></button> </td>
	 <td> <button onclick="calculate()"><b> = </b></button> </td>
       </tr>
     </table>
    </div>
   </div>

<script>
         function appendToDisplay(value) {
    document.getElementById('display').value += value;
}

function clearDisplay() {
    document.getElementById('display').value = '';
}

function calculate() {
    var display = document.getElementById('display');
    try {
        display.value = eval(display.value);
    } catch (error) {
        display.value = 'Error';
    }
}
</script>

  </body>
 </html>
