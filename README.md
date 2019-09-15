# Heart Rate Monitor

## Introduction 
Create a program that can monitor your heart rate. Show your ``||gatorParticle: heart rate||`` on the micro:bit and have the ``||Neopixel: 5 LEDS||`` on the gator:bit blink according to their heart rate. After you think you've figured it out, ``|Download|`` the code and test it out. 

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(gatorParticle.heartbeat(HeartbeatType.BPM))
})
gatorParticle.begin()
let strip = neopixel.create(DigitalPin.P12, 5, NeoPixelMode.RGB)
basic.forever(function () {
    strip.showColor(neopixel.colors(NeoPixelColors.Purple))
    basic.pause(gatorParticle.heartbeat(HeartbeatType.BPM))
    strip.clear()
    strip.show()
    basic.pause(gatorParticle.heartbeat(HeartbeatType.BPM))
})
```

```package
gatorParticle=github:sparkfun/pxt-gator-particle
```





