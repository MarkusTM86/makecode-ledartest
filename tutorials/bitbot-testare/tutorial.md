# BitBot: Testare för ledare

# package
bitbot=github:4tronix/BitBot

## Steg 1

Nu ska vi använda ett block för vad som ska hända när en krets sluts.

```blocks
input.onPinPressed(TouchPin.P0, function () {

})
input.onPinReleased(TouchPin.P0, function () {

})
bitbot.motor(BBMotor.All, 100)
bitbot.stop(BBMotor.All)
basic.showIcon(IconNames.Heart)
basic.showIcon(IconNames.No)
```

## Steg 2

Lägg till något som händer när Pin0 trycks, t.ex. köra framåt och visa hjärta.

```blocks
input.onPinPressed(TouchPin.P0, function () {
    bitbot.motor(BBMotor.All, 100)
    basic.showIcon(IconNames.Heart)
})
```

## Steg 3

Lägg till ett block för när Pin0 släpps – stanna BitBot och visa kryss.

```blocks
input.onPinReleased(TouchPin.P0, function () {
    bitbot.stop(BBMotor.All)
    basic.showIcon(IconNames.No)
})
```

## Steg 4

Testa olika material genom att koppla en ledare mellan GND och Pin0.

Fungerar:
- Aluminiumfolie
- Mynt
- Våt trasa

Fungerar inte:
- Plast
- Papper
- Trä
