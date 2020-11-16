# Accelerationsensor

## Step 1

Drag the ``||Basic:on start||`` block to the trash on the left main menu.

In ``||Variables:Variables||``, create a variable and call it: ``||Variables:Absolute Acceleration||``
 
## Step 2
In ``||Variables:Variables||``, drag the ``||Variables:set Absolute_Acceleration to 0||`` block inside the ``||Basic:Forever||`` block
```blocks
basic.forever(function(){
Absolute_Acceleration = 0
})
```
 
## Step 3
In ``||Led:Led||``, drag the ``||Led:plot bar graph of 0 up to 0||`` block under the ``||Variables:set Absolute_Acceleration to 0||`` block
```blocks
basic.forever(function(){
Absolute_Acceleration = 0
led.plotBarGraph(0,0)
})
```
 
## Step 4
In ``||Input:Input||``, drag the ``||Input:acceleration (mg) x||`` block and replace the "0" inside the ``||Variables:set Absolute_Acceleration to 0||``
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.x)
led.plotBarGraph(0,0)
})
```
 
## Step 5
Click on the down arrow of the ``||Input:acceleration (mg) x||`` and change the "x" to ``||Input:acceleration (mg) strength||``
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(0,0)
})
```

## Step 6
In ``||Variables:Variables||``, drag the ``||Variables:Absolute Acceleration||`` block and replace the first 0 inside the ``||Led:plot bar graph of 0 up to 0||`` block.
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumber(0)
})
```

## Step 7
On the left menu. click down ``||Advanced:Advanced||`` arrow. Then, in ``||Serial:Serial||`` "Serial", drag the ``||Serial:serial write number 0||`` block under the previous ``||Led:plot bar graph of 0 up to 0||`` block
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumber(0)
})
```
 
## Step 8
In ``||Variables:Variables||``, drag the ``||Variables:Absolute Acceleration||`` red block and replace the 0 inside the ``||Serial:serial write number 0||`` block.
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumber(Absolute_Acceleration)
})
```
 
## Step 9
Connect the Micro:bit to the USB port on your computer. Then click on ``||LED:Download||`` (Make sure that you download the file to the Micro:bit drive")
```blocks
basic.forever(function(){
Absolute_Acceleration = input.acceleration(Dimension.Strength)
led.plotBarGraph(Absolute_Acceleration,0)
serial.writeNumber(Absolute_Acceleration)
})
```
## Step 10
Congratulations, you did it!

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
