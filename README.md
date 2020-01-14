# JAVASCRIPT_Basics
Exercise1:Write a JavaScript program to display the current day and time in the following format. 
Sample Output : Today is : Tuesday.
Current time is : 10 PM : 30 : 38

Code:const readline=require('readline-sync');

var date=new Date();
var day=date.getDay();
var daylist=["Sunday","Monday","Tuesday","Thursday","Friday","Saturday"]

var hour= date.getHours();
var min=date.getMinutes();
var sec=date.getSeconds();
var ampm=hour  >= 12? 'PM':'AM';
hour=hour>=12?hour-12:hour;

if(hour===0 && min==='PM'){
  if(min===0 && sec===0){
    hour=12;
    ampm='noon'
  }
  else{
    hour=00;
    ampm="AM";
  }
}


console.log("Today is:"+daylist[day]);
console.log("Current Time: "+ hour + ampm + " : " +min+" : "+sec);
=================================================================

Exercise2:Write a JavaScript program to print the contents of the current window
============
Code
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Print the content of current page</title>
    <script type="text/javascript">
      function printContent(){
        window.print();
      }
      
      
    </script>
  </head>
  <body>
    <h1>This is a Practice page</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    <button type="button" name="button" onclick="printContent()">Print this page</button>
  </body>
</html>

=========================================================================
 Write a JavaScript program to get the current date.
 ============
code:
const readline=require('readline-sync');
function dateFormate(){
   var date=new Date();
    var year=date.getFullYear();
    var mon=(1+date.getMonth()).toString().padStart(2,'0');
     var day=date.getDate();
     day=day>=10? day.toString().padStart(2,'0'):day;



return(day+" / "+mon+" / "+year); };console.log(dateFormate());

Exercise 4 :Write a JavaScript program to find the area of a triangle where lengths of the three of its sides are 5, 6, 7
======

Code:const readline=require('readline-sync');
function areaTriangle(a,b,c) {
  //area of triangle with 3 sides=square root of(s(s-a)(s-b)(s-c)) where s=(a+b+c)/2
  var area;
  var s=(a+b+c)/2;
  return area=Math.sqrt(s*(s-a)*(s-b)*(s-c));



}
console.log(areaTriangle(5,6,7));
=

