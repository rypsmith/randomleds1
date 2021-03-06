# Random LEDs ON!

## Introduction @unplugged

How can you turn on the LEDs on the micro:bit randomly like this:

![Heart shape in the LEDs](https://raw.githubusercontent.com/rypsmith/randomleds1/master/randomledson.gif)

Follow the steps to start to learn how to use the ``||math:pick random||`` block.

## Step 1 - Plot random!

Get a ``||led:plot||`` block and place it inside of the forever block.
    
```blocks
basic.forever(function() {
    led.plot(0,0)
})
```

```ghost
led.plot(0,0)
```

## Step 2 - Turn on a single LED

Adjust either the x or y coordinate in the ``||led:plot||`` block to turn on one LED.

![XY Coordinates on micro:bit](https://rypsmith.github.io/randomleds1/displayxycoords.png)

## Step 3 - bring in some randomness!

Get a ``||math:pick random||`` block and insert in twice (two times) into the x and y value in the ``||led:plot||`` block

```blocks
basic.forever(function() {
    led.plot(randint(0, 10),randint(0, 10))
})
```

```ghost
math.random(0,0)
```

## Step 4 - adjust the range

Since the LEDs are an array (list of values) from 0 to 4, fix the ``||math:random||`` block to be between 0 and 4. Remember press run to see it work!

```blocks
basic.forever(function() {
    led.plot(randint(0, 4),randint(0, 4))
})
```

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
