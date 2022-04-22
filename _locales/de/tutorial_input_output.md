# Input-Output

## Aufgabenstellung

Am LED-Display des BBC micro:bit soll 
- beim Start der Text "Hi!" augegeben werden
- beim Drücken von Button A ein lachender Smiley angezeigt werden
- beim Drucken von Button B ein trauriger Smiley angezeigt werden
- ein großes Herz angezeigt werden, nachdem der BBC micro:bit geschüttelt wurde

## Schritt 1

Ausgabe Text "Hi!"

```blocks
basic.showString("Hi!")
```
## Schritt 2

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showIcon(IconNames.Happy)
})
```

## Schritt 3

```blocks
input.onButtonPressed(Button.B, function () {
    basic.showIcon(IconNames.Sad)
```

## Schritt 4

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
})
```
## Gesamter Programmcode:

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