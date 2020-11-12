# Accelerationsensor
## Step 1
In "Variables", create "Absolute Acceleration"
 
## Step 2
In "Variables", drag the "set Absolute_Acceleration" block inside the "Forever" block
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
})
```
 
## Step 3
In "Led", drag the "plot bar graph of 0 up to 0" block under the previous block
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(0,0)
})
```
 
## Step 4
In "Input", drag the "acceleration (mg) strength" block and replace the "0" inside the "set Absolute_Acceleration to 0"
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
})
```
 
## Step 5
In "Serial", drag the "serial write numbers array of 0 1" block under the "plot bar graph of Absolute_Acceleration up to 0" block
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumbers([0,1])
})
```
 
## Step 6
click on the "-" next to the "0"
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumbers([0])
})
```
 
## Step 7
In "Input", drag the "acceleration (mg) strength inside the array of 0" and replace the "0"
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumbers([Absolute_Acceleration])
})
```
 
## Step 8
Connect the Micro:bit to the USB port on your computer. Then click on "Download" (Make sure that you download the file to the Micro:bit drive")
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumbers([Absolute_Acceleration])
})
```
 
## Step 9
Congratulations, you did it!

