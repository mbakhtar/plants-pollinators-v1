# Plants & Pollinators

## @showhint
```package
cakLand=github:climate-action-kits/pxt-climate-action-kit-land
```
Create a variable. Go to ``||Variables:Variables||`` click on Make a Variable. 
Name the Variable ``||Variables:bugVisits||``

## @showhint
Now under ``||Variables:Variables||`` drawer ``||Variables:bugVisits||`` exists 
and three additional blocks are available.

## @showhint
Add ``||basic:showNumber||`` under ``||basic:on start||`` block
```blocks
basic.showNumber()
```
## @showhint
Add ``||Variables:set bugVisits to 0||`` to ``||basic:on start||`` block
```blocks
let bugVisits = 0
basic.showNumber()
```
## @showhint
Add ``||logic:if true||`` conditional block under the ``||basic:forever||`` loop
```blocks
let bugVisits = 0
basic.showNumber()
basic.forever(function ()
{ if (true)}

```
## @showhint
Now add ``||Variables:change bugVisits by 1||`` everytime ``||cakLandTouch:Touch Sensor||`` is activated
```blocks
let bugVisits = 0
basic.showNumber(bugVisits)
basic.forever(function () {
    if (cakLandTouch.getTouch(cakLandTouch.TouchPin.P12)) {
        bugVisits += 1
    }
})
```
## @showhint
The last step is to show the number on the micro:bit's LED display. 
Add ``||basic.showNumber||`` block and 
drag the ``||Variables:bugVisits||`` and 
place it in the oval space
```blocks
let bugvisits = 0
basic.showNumber(bugvisits)
basic.forever(function () {
    if (cakLandTouch.getTouch(cakLandTouch.TouchPin.P12)) {
        bugvisits += 1
        basic.showNumber(bugvisits)
    }
})
```
