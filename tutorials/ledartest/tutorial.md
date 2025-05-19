# Testare: Ledare eller isolator?

## Steg 1: Vad ska vi bygga?
Vi ska bygga ett enkelt verktyg som testar om ett material är **ledande** eller en **isolator**.

Vi använder krokodilklämmor mellan **GND** och **Pin0**.

Om ström kan gå genom materialet → vi ser ett hjärta ❤️  
Annars → vi ser ett kryss ❌

## Steg 2: När pin0 trycks
Gå till **Ingång** (Input) och dra in blocket [||input:on pin P0 pressed||].

Detta block körs varje gång micro:bit känner att **Pin0** trycks, vilket händer när ström går genom materialet.

## Steg 3: Visa symbol för ledare
Inuti `när pin0 trycks`-blocket, gå till **Grundläggande** och dra in blocket [||basic:show icon||].

Välj hjärtat ❤️ som ikon.

## Steg 4: Visa symbol för isolator
Gå till **Ingång** och dra in blocket [||input:on pin P0 released||].

Inuti detta block, dra in [||basic:show icon||] och välj kryss ❌ som ikon.

## Steg 5: Testa!
Anslut två krokodilklämmor:
- En till **GND**
- En till **Pin0**

Tryck fast dem på varsin sida av ett material.  
Testa t.ex. **aluminiumfolie**, **mynt**, **plast**, **trä**, **papper**...

## Bonus: Lägg till ljud
Vill du lägga till ljud för ledare?

Inuti `när pin0 trycks`-blocket, gå till **Musik** och dra in blocket [||music:play tone Middle C for 1 beat||].

Nu får du både ljud och ikon!

## Klar!
Grattis! Du har skapat ett verktyg som testar material.

Lär dig mer: Vad är elektroner? Varför leder metall men inte plast?
