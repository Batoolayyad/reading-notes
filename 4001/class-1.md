## Describe (in plain English) what Array.map() does:


creates new array has the results of calling a provided function on every element in the calling array.


## Describe (in plain English) what Array.reduce() does


executes a reducer function (that you provide) on each element of the array, and return a single output value.


## Provide code snippets showing how to use superagent() to fetch data from a URL and log the result


### With normal Promise .then() syntax

```
function getCharacters(){
  superagent.get('https://swapi.dev/api/people/')
  .then(data=>{
   data.body.results.forEach(character=>{
    console.log(character)
    })
  });
}
getCharacters()

```
### Again with async / await syntax


``` 
async function getCite(cityName){
  let result=await superagent.get(`https://geocode.xyz/${cityName}?json=1`)
  console.log(`${cityName}: longitude ${result.body.longt}, latitude ${result.body.latt}`)
  }
 getCite(amman)

```


## Explain promises as though you were mentoring a Code 301 level student


Promises are one way to manage Asynchronous actions, the code keep running skip and when it reach a line that need time it skip it and when the data is ready bring it back to the line where it was asked for it.


## Are all callback functions considered to be Asynchronous? Why or Why Not?


first lets see the definition of a callback function, a  callback function is a function that gets passed as an argument into a parent function call.
A callback can be used synchronously or asynchronously depends on the order in which things happen in the timeline.
