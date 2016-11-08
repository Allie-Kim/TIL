# Tips of Chrome Developer Console

#### to edit text in the broswer itself
````javascript
document.body.contentEditable=true
````

#### to get events associated with an element
````javascript
getEventListeners($('selector'))
````

#### to get the time of execution of a code block
````javascript
**console.time('myTime');**
for(var i=0; i < 100000; i++){
  2+4+5;
}
**console.timeEnd('mytime');**
//Output - myTime:12345.00 ms
````

#### to get values to table
>var myArray=[{a:1,b:2,c:3},{a:1,b:2,c:3,d:4},{k:11,f:22},{a:1,b:2,c:3}]

````javascript
console.table(myArray)
````