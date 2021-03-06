# Gam3pad
Easy and convenient way to use the Gamepad API

<br>

## How to use Gam3pad


```
npm install gam3pad
```
 
```js
import { Gam3pad } from 'gam3pad'

const gamepad = new Gam3pad()

gamepad.on(Gam3pad.INPUT.R1, data => {
  console.log(data)
})
```

<br>

## API Docs

```js
//Static property that contains of all of the possible types
static INPUT: object

//Listen for events and invoke the callback function 
//when one happens based on the type provided
on(type: string, cb: Function): void

//Function that allows for vibration of the gamepad
//delay and duration combined must be less than 5000
vibrate({
  delay?: number, //Amount of time in ms to delay the vibrate by (min: 1, max: 5000)
  duration?: number, //Amount of time in ms to vibrate the gamepad (min: 1, max: 5000)
  weak?: number, //Amount of force to apply the weak vibrator with (min: 0, max: 1)
  strong?: number //Amount of force to apply the strong vibrator with (min: 0, max: 1)
}): void
```

<br> 

## Available types

### Global
```js
//when a controller has been connected
Gam3pad.INPUT.CONNECTED

//when a controller has been disconnected
Gam3pad.INPUT.DISCONNECTED

//when joysticks have been used
Gam3pad.INPUT.JOYSTICKS

//when any input has happened
Gam3pad.INPUT.ALL
```

### Standard Layout
```js
Gam3pad.INPUT.L1
Gam3pad.INPUT.R1
Gam3pad.INPUT.L2
Gam3pad.INPUT.R2
Gam3pad.INPUT.L3
Gam3pad.INPUT.R3
Gam3pad.INPUT.UP
Gam3pad.INPUT.DOWN
Gam3pad.INPUT.LEFT
Gam3pad.INPUT.RIGHT
Gam3pad.INPUT.HOME
Gam3pad.INPUT.START
Gam3pad.INPUT.SELECT
Gam3pad.INPUT.BUTTON_UP
Gam3pad.INPUT.BUTTON_DOWN
Gam3pad.INPUT.BUTTON_LEFT
Gam3pad.INPUT.BUTTON_RIGHT
```
