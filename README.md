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
