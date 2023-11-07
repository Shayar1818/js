# js
```
EXPERIMENT NO : 01

--------------------------CODE-----------------------


<html>
<head>
<title> Experiment No 1</title>
<script src ="exp1.js"></script>
</head>
<h1> Area of Triangle</h1>
<body>
<label> Enter the Base</label>
<input id ="base">
<br>
<br>
<label> Enter the Height</label>
<input id ="Height">
<br>
<br>
<button type="submt" onclick="Triangle()">Compute</button>
<br>
<h3 id="try">Triangle Output</h3>
<br>
<br>
<head>
<script src ="exp1.js"></script>
</head>
<h1> Area of Rectangle</h1>
<body>
<label> Enter the Length</label>
<input id ="Length">
<br>
<br>
<label> Enter the Breadth</label>
<input id ="Breadth">
<br>
<br>
<button type="submt" onclick="Rectangle()">Compute</button>
<br>
<h3 id="cal">Rectangle Output</h3>
<br>
 
<br>
<br>
<br>
<head>
<script src ="exp1.js"></script>
</head>
<h1> Area of Circle</h1>
<body>
<label> Enter the radius</label>
<input id ="radius">
<br>
<br>
<button type="submt" onclick="Circle()">Compute</button>
<br>
<h3 id="result">Circle Output</h3>
<br>
<br>
</body>
</head>
</html>


function Triangle()
{
var b=parseFloat(document.getElementById("base").value); var h=parseFloat(document.getElementById("Height").value); var a=0.5*b*h;
document.getElementById("try").innerHTML="Area of Triangle : " +a;
}
function Rectangle()
{
var l=parseFloat(document.getElementById("Length").value); var b=parseFloat(document.getElementById("Breadth").value); var a=l*b;
document.getElementById("cal").innerHTML="Area of Triangle : " +a;
}
function Circle()
{
var r=parseFloat(document.getElementById("radius").value); var a= 3.14*r*r;
document.getElementById("result").innerHTML="Area of Circle : " +a;
 
EXPERIMENT NO : 02
--------------------------CODE-----------------------


<html>
<head>
<title> Experiment No 2</title>
<script src ="exp2.js"></script>
</head>
<h1> Create table</h1>
<body>
<label> Enter the Number</label>
<input id ="base">
<br>
<br>

<button type="submt" onclick="Multiple()">Compute</button>
<br>
<h3 id="try"></h3>
<br>
<br>
</body>
</html>


function Multiple()
{
var b=parseFloat(document.getElementById("base").value); for(var i=1; i<=10; i++){

document.getElementById("try").innerHTML +=b +" X "+i+" = "+ b * i + "<br/>";
}
}
 
EXPERIMENT NO : 03
--------------------------CODE-----------------------

<html>
<head>
<title> Experiment No 3</title>
</head>
<h1> String Operations</h1>
<br>
<body>
<label> Enter the Sring</label>
<input id ="base">
<br>
<br>
<h2> Using for Loop</h2>
<button type="submt" onclick="reverse()">Reverse</button>
<h3 id="try"></h3>
<br>
<h2> Using Built in function</h2>
<button type="submit" onclick="bultin()">Reverse</button>
<h3 id="me"></h3>
<br>
<h2> Using Replace function</h2>
<br>
<label> Enter the Charcater to be Remove</label>
<input id ="remove">
<br>
<br>
<label>Enter the Charcater to be Added</label>
<input id ="add">
<br>
<br>
<button type="submit" onclick="rep()">Replace & add</button>
<h3 id="result1"></h3>
<h2> Using Replaceall function</h2>
<br>
<br>
<label> Enter the Charcater to be Remove</label>
<input id ="remov">
<br>
 
<br>
<label>Enter the Charcater to be Added</label>
<input id ="ad">
<br>
<br>
<button type="submit" onclick="repall()">Replace & add</button>
<h3 id="result2"></h3>
<br>
<h2> Check String is Palindrome or Not </h2>
<button type="submit" onclick="check()">Check</button>
<h3 id="result3"></h3>
<script>
// Using For loop function reverse()
{
var str=(document.getElementById("base").value); let reversedStr = "";
for (let i = str.length - 1; i >= 0; i--) { reversedStr += str[i];
}
document.getElementById("try").innerHTML ="Reverse String is "+ reversedStr; return reversedStr;

}
// Built in Function function bultin(){
var str=(document.getElementById("base").value); const arr=str.split("");
const arr1=arr.reverse(); const join=arr1.join("");
document.getElementById("me").innerHTML ="Reverse String is "+ join;

}

function rep(){
var   str=(document.getElementById("base").value); var str1=(document.getElementById("remove").value); var str2=(document.getElementById("add").value);
var newstr=str.replace(str1, str2); document.getElementById("result1").innerHTML ="New String is "+ newstr;



}
function repall(){
var str=(document.getElementById("base").value); var str1=(document.getElementById("remov").value);
 
var str2=(document.getElementById("ad").value); var newstr1=str.replaceAll(str1,str2);
document.getElementById("result2").innerHTML ="New String is "+ newstr1;
}

function check()
{
var str=(document.getElementById("base").value); var str1=reverse();
if(str==str1){
document.getElementById("result3").innerHTML =" String is Palindrome ";
}
else{
document.getElementById("result3").innerHTML =" String is not Palindrome ";
}

}
</script>
</body>
</html>
 
EXPERIMENT NO : 04
--------------------------CODE-----------------------
<html>
<head>
<title> Experiment No 3</title>
</head>
<h1> String Comparison </h1>

<br>
<body>
<h3> <label>Enter the first String</label>
<input id ="firststr"></h3>


<h3><label>Enter the Second String</label>
<input id ="secondstr"></h3>

<br>

<h2> Mathematical Operations</h2>
<br>
<button type="submit" onclick="compare()">Compare</button>
<h4 id="try"></h4>
<br>

<h2> Strict Equality Operator</h2>
<br>
<button type="submit" onclick="strictequality()">Compare</button>
<h4 id="result"></h4>
<br>

<h2> Using match method</h2>
<br>
<button type="submit" onclick="match()">Compare</button>
<h4 id="result1"></h4>
<br>

<h2> Using matchAll method</h2>
<br>
<button type="submit" onclick="matchall()">Compare</button>
<h4 id="result2"></h4>
<br>
<h2> Using localeCompare method</h2>
<br>
<button type="submit" onclick="localcompare()">Compare</button>
 
<h4 id="result3"></h4>


<script>
function compare()
{
var str1=(document.getElementById("firststr").value); var str2=(document.getElementById("secondstr").value); if(str1>str2)
{
document.getElementById("try").innerHTML =" String 1 is greater then String 2 ";
}
else if(str1<str2){
document.getElementById("try").innerHTML =" String 2 is greater then String 1";
}
else{
document.getElementById("try").innerHTML ="Both String are equal "
}
}
function strictequality()
{
var   str1=(document.getElementById("firststr").value); var str2=(document.getElementById("secondstr").value); if(str1===str2)
{
document.getElementById("result").innerHTML ="Both String are equal ";
}
else{
document.getElementById("result").innerHTML ="String are not Equal";
}
}
function match()
{
var   str1=(document.getElementById("firststr").value); var str2=(document.getElementById("secondstr").value); let result= str1.match(str2);
var cmp ;
let y=str1.indexOf(result); if(result!=str2){
cmp="String 1 is not macthing with string 2";
}
else
{
cmp="String 1 is matching with string 2 <br>Index : "+y+"<br>"+" Element : "+ result;
}
document.getElementById("result1").innerHTML = cmp ;
}


function matchall()
{
 
var str1=(document.getElementById("firststr").value); var str2=(document.getElementById("secondstr").value); var cmp;
var result=str1.matchAll(str2); var y=" ";
for(var x of result)
{
y=y+x.index + " "

}
if(x!=str2){
cmp="String 1 is not matching with string 2";
}
else{
cmp="String 1 is matching with string 2 <br>Index : "+y+"<br>"+" Element : "+ x;
}
document.getElementById("result2").innerHTML = cmp ;

}

function localcompare()
{
var str1=(document.getElementById("firststr").value); var str2=(document.getElementById("secondstr").value); var str3=str1.localeCompare(str2);
var cmp; if(str3==0)
{
cmp=str3+ ", Means string 1 is equal to string 2 ";
}
else if(str3==-1)
{
cmp=str3+", Means string 2 is gerater then string 1";
}
else{
cmp=str3+", Means String 1 is gerater then string 2";
}
document.getElementById("result3").innerHTML = cmp ;
}

</script>
 
EXPERIMENT NO : 05



---------------------------------------------CODE--------------------------------------------


<html>
<head>
<title>Countdown Timer</title>
</head>
<body>
<div class="timer-container">
<h1>Countdown Timer</h1>
<h2><label	for="expiry-input">Enter	Timer	Expiry	Date	and	Time	(YYYY-MM-DD HH:MM:SS):</label></h2>
<input type="text" id="expiry-input" placeholder="YYYY-MM-DD HH:MM:SS">
<button id="start-button">Start Countdown</button>
<div class="timer">
<br>
<br>
<h1 id="days">00 : 00 : 00 : 00</h1>
<h1 id="me">Message Loading	</h1>
</div>
</div>
<script src="script.js"></script>
</body>
</html>
 
let expiryDate = 0; let timerInterval;
document.getElementById("start-button").addEventListener("click", function () { const inputDate = document.getElementById("expiry-input").value;
const parsedDate = new Date(inputDate).getTime();
if (!isNaN(parsedDate) && parsedDate > new Date().getTime()) { expiryDate = parsedDate;
clearInterval(timerInterval);
timerInterval = setInterval(updateTimer, 1000);
} else {
document.getElementById("me").textContent = "Please enter a valid future date and time.";
}
});


function updateTimer() {
const currentDate = new Date().getTime(); const diﬀerence = expiryDate - currentDate; if (diﬀerence <= 0) {
clearInterval(timerInterval); document.getElementById("me").textContent = "WELCOME RITIk";
} else {
const days = Math.ﬂoor(diﬀerence / (1000 * 60 * 60 * 24));
const hours = Math.ﬂoor((diﬀerence % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
const minutes = Math.ﬂoor((diﬀerence % (1000 * 60 * 60)) / (1000 * 60)); const seconds = Math.ﬂoor((diﬀerence % (1000 * 60)) / 1000);
document.getElementById("days").textContent = days + " : " + hours + " : " + minutes + " : " + seconds;
}
}
 
EXPERIMENT NO : 06
---------------------------------------------CODE--------------------------------------------
<html>
<head>

<title> Experiment No 6</title>


</head>
<h1> Array Operations</h1>

<body>
<label> Enter Array Element </label>
<input id ="arr">

<br>
<button type="submt" onclick="arrayfrom()">Dispaly</button>	<br>
<h3 id="try"></h3>
<br>

<label> Enter Element to be Remove</label>
<input id = "Remove">
<br>
<button type="submt" onclick="remove()">Remove</button>	<br>
<h3 id="try1"></h3>
<br>

<label> Enter Element to be Check</label>
<input id = "check">

<br>
<button type="submt" onclick="check()">Check</button>	<br>
 
<h3 id="try2"></h3>
<br>
<label> Empty Array</label>
<input id = "empty">

<br>
<button type="submt" onclick="empty()">Empty</button>
<br>
<h3 id="try3"></h3>




<script>

function arrayfrom(){
var x=(document.getElementById("arr").value); var arr= x.split(',');
document.getElementById("try").innerHTML ="Array is "+ arr;




}


function remove(){
var x=(document.getElementById("arr").value); var arr= x.split(',');
var y=(document.getElementById("Remove").value); var i=arr.indexOf(y);
var myarray= arr.splice(i,1);


document.getElementById("try1").innerHTML ="Array After Removing Element "+ arr;


}


function check(){
 
var x=(document.getElementById("arr").value); var arr= x.split(',');
var y=(document.getElementById("check").value); var i=arr.indexOf(y);
if(i==-1){


document.getElementById("try2").innerHTML ="Element not present in array ";

}
else{

document.getElementById("try2").innerHTML ="Element is present at index :" +i;
}

}
function empty(){
var x=(document.getElementById("empty").value); var arr= x.split(',');
arr.length=0;

document.getElementById("try3").innerHTML ="Array is Empty "+ arr;
}


</script>
</body>

</html>
 
EXPERIMENT NO : 07



---------------------------------------------CODE--------------------------------------------
<html>


<title>Experiment No:7</title>

<head>


<h1>Object Array Demo</h1>
</head>
<body>
<br>
<h2><label for="field">Field:</label>

<input type="text" id="field"></h2>
<br>
<h2><label for="value">Value:</label>

<input type="text" id="value"></h2>
<br>

<button onclick="addObjectToArray()">Add to Array</button>
<br>

<h2>Array Contents:</h2>
<h2 id="output"></h2>
<br>
<h2><label for="checkVariable">Check Variable:</label>
<input type="text" id="checkVariable"></h2>

<br>
<br>
<button onclick="checkInArray()">Check in Array</button>
 
<br>
<h2 id="result"></h2>


<script >

var objectArray = [];


// Function to add an object to the array function addObjectToArray() {
var field = document.getElementById("field").value; var value = document.getElementById("value").value;

// Create an object with the given field and value var newObject = { field: field, value: value };

// Add the object to the array objectArray.push(newObject);


// Clear input fields document.getElementById("field").value = ""; document.getElementById("value").value = "";

// Display the updated array displayArray();
}
function displayArray() {

var output = document.getElementById("output"); output.innerHTML = "";


objectArray.forEach(function(obj) {
var listItem = document.createElement("li"); listItem.textContent = JSON.stringify(obj);
 
output.appendChild(listItem);

});

}


// Function to check if a variable is in the array function checkInArray() {
var variableToCheck = document.getElementById("checkVariable").value;


// Check if the variable is in the array

var isInArray = objectArray.some(function(obj) { return obj.field === variableToCheck;
});


var result = document.getElementById("result"); if (isInArray) {
result.textContent = "Variable is in the array.";

} else {
result.textContent = "Variable is not in the array.";
}
}
</script>

</body>
 
EXPERIMENT NO : 08



---------------------------------------------CODE--------------------------------------------
<html>

<head>
<title> Experiment No 8</title>

</head>
<body>

<h1 style="text-align: center;"><u>Experiment No: 8</u></h1>
<br>
<div id="div1" style="height: 100px; width: 100%; background-color:blueviolet" onmousemove="changeDivColor();"
onmouseout="this.style.backgroundColor='blue'">
<h3 style="text-align: center;"><u>Mouseover</u></h3> </div>
<br>
<br>
<br>

<div style="text-align: center; height: 100px;width: 100%; background-color:grey" >
<a style="height: 100%; width: 100%;" href="https://www.google.com" target="blank" onfocus="this.style.backgroundColor='blue'"
onblur="this.style.backgroundColor='red'">Onfocus</a>

</div>
<script>
function changeDivColor(){ div1.style.backgroundColor="grey";
}

</script>
</body>


 
EXPERIMENT NO : 09



---------------------------------------------CODE--------------------------------------------


<html>
<head>

<title> Experiment No 9</title>
</head>

<body>
<h1> Calculator Program in JavaScript </h1>
<div class= "formstyle">
<form name = "form1">
<input id = "calc" type ="text" name = "answer"> <br> <br>

<input type = "button" value = "1" onclick = "form1.answer.value += '1' ">
<input type = "button" value = "2" onclick = "form1.answer.value += '2' ">
<input type = "button" value = "3" onclick = "form1.answer.value += '3' ">

<input type = "button" value = "+" onclick = "form1.answer.value += '+' ">
<br> <br>


<input type = "button" value = "4" onclick = "form1.answer.value += '4' ">

<input type = "button" value = "5" onclick = "form1.answer.value += '5' ">
<input type = "button" value = "6" onclick = "form1.answer.value += '6' ">
<input type = "button" value = "-" onclick = "form1.answer.value += '-' ">
<br> <br>


<input type = "button" value = "7" onclick = "form1.answer.value += '7' ">
<input type = "button" value = "8" onclick = "form1.answer.value += '8' ">
<input type = "button" value = "9" onclick = "form1.answer.value += '9' ">
 
<input type = "button" value = "*" onclick = "form1.answer.value += '*' ">
<br> <br>




<input type = "button" value = "/" onclick = "form1.answer.value += '/' ">
<input type = "button" value = "0" onclick = "form1.answer.value += '0' ">
<input type = "button" value = "." onclick = "form1.answer.value += '.' ">

<!-- When we click on the '=' button, the onclick() shows the sum results on the calculator screen. -
->

<input type = "button" value = "=" onclick = "form1.answer.value = eval(form1.answer.value) ">
<br> <br>
<!-- Display the Cancel button and erase all data entered by the user. -->
<input type = "button" value = "Clear All" onclick = "form1.answer.value = ' ' " id= "clear" >

<br>


</form>
</div>

</body>
 
EXPERIMENT NO : 10



---------------------------------------------CODE--------------------------------------------


<!DOCTYPE html>
<html>

<head>
<title>Experiment No 10</title>

</head>
<body>
<h1>JavaScript Properties</h1>
<h3 id="browserInfo"></h3>
<h3 id="screenInfo"></h3>

<h3 id="historyInfo"></h3>
<h3 id="paragraphCount"></h3>
<h3 id="replaceText">Original Text</h3>

<script>
const browserInfo = `Browser Name: ${navigator.appName}, Version: ${navigator.appVersion}`; document.getElementById('browserInfo').textContent = browserInfo;
const screenInfo = `Screen Width: ${window.screen.width}, Screen Height: ${window.screen.height}`; document.getElementById('screenInfo').textContent = screenInfo;
const historyInfo = `History Length: ${window.history.length}`; document.getElementById('historyInfo').textContent = historyInfo;
const paragraphCount = document.getElementsByTagName('p').length;
document.getElementById('paragraphCount').textContent = `Number of <p> tags:
${paragraphCount}`;
const replaceTextElement = document.getElementById('replaceText'); replaceTextElement.textContent = 'Replaced Text';
 
</script>
</body>
</html>


```
