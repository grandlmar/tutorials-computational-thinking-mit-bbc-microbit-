# Input-Output

## Aufgabenstellung

Am LED-Display des BBC micro:bit soll 
- beim Start der Text "Hi!" augegeben werden
- beim Drücken von Button A ein lachender Smiley angezeigt werden
- beim Drucken von Button B ein trauriger Smiley angezeigt werden
- ein großes Herz angezeigt werden, nachdem der BBC micro:bit geschüttelt wurde

## Schritt 1

Am LED-Display des BBC micro:bit soll **beim Start** der Text "Hi!" augegeben werden
Wähle dazu einen passenden Befehl aus der Kategorie **Grundlagen**.

```blocks
basic.showString("Hi!")
```
## Schritt 2

Wenn **Knopf A** gedrückt wird, dann soll am **LED-Display** ein **lachender Smiley** angezeigt werden.

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showIcon(IconNames.Happy)
})
```

## Schritt 3

Wenn **Knopf B** gedrückt wird, dann soll am **LED-Display** ein **trauriger Smiley** angezeigt werden.

```blocks
input.onButtonPressed(Button.B, function () {
    basic.showIcon(IconNames.Sad)
```

## Schritt 4

Wenn der BBC micro:bit **geschüttelt** wird, dann soll am **LED-Display** ein **großes Herz** angezeigt werden.

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
})
```
## Gesamter Programmcode:

Sieh dir den gesamten Programmcode an:

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