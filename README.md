# Timers-Exercise
UMass Web Fundamentals Timers Exercise

```js
// Countdown

/* Write a function called countdown that accepts a number as a parameter and every 1000 milliseconds decrements the value and console.logs it. Once the value is 0 it should log "DONE!" and stop.*/

function countdown(time) { // Had to look at solution because I couldn't understand whats going on
  let timer = setInterval(function() {
    time--;
    if(time <= 0){
      clearInterval(timer);
      console.log("DONE!");
    }
    else{
      console.log(time);
    }
  }, 1000);
}

function randomGame(){ // Thank you previous example for showing me how to do this!
  let tries = 0;
  let game = setInterval(function() {
    tries++;
    let randomNumber = Math.random();
    if(randomNumber > .75){
      clearInterval(game);
      console.log(tries);
      console.log(`It took ${tries} amount of tries for the random number to exceed .75`);
    }
    else{
      console.log(tries);
    }
  }, 1000);
}

randomGame();
```
