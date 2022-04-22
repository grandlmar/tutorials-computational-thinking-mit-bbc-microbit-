# Tutorial: Input-Output
## Schritt 1

Am LED-Display des BBC micro:bit soll 
- beim Start der Text "Hi!" augegeben werden
- beim Drücken von Button A ein lachender Smiley angezeigt werden
- beim Drucken von Button B ein trauriger Smiley angezeigt werden
- ein großes Herz angezeigt werden, nachdem der BBC micro:bit geschüttelt wurde

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showIcon(IconNames.Happy)
})
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
})
input.onButtonPressed(Button.B, function () {
    basic.showIcon(IconNames.Sad)
})
basic.showString("Hi!")
```