# Led-pasek

## ZADÁNÍ:
#### Jako ročníkový projekt jsem si vybral LED pásek, který bude umět měnit barvu světla, intenzitu světla a další různé světelné efekty které zvládnu nahrát. 

## POPIS PRÁCE:
#### Nejprve jsem si koupil Arduino UNO R3 na kterém programuji, dále jsme si s kolegou Tomášem Jarkovským oba zakoupili LED programovací pásek na stránce TEMU, abychom měli levnejší poštovné. Programuji pomocí AI, který mi pomáhá abych pochopil začátek tohoto projektu. 

## PROGRAM: 
#### #include <FastLED.h>

#define LED_PIN     7
#define NUM_LEDS    20

CRGB leds[NUM_LEDS];

void setup() {

  FastLED.addLeds<WS2812, LED_PIN, GRB>(leds, NUM_LEDS);

}

void loop() {

  for (int i = 0; i <= 19; i++) {
    leds[i] = CRGB ( 0, 0, 255);
    FastLED.show();
    delay(40);
  }
  for (int i = 19; i >= 0; i--) {
    leds[i] = CRGB ( 255, 0, 0);
    FastLED.show();
    delay(40);
  }
}
##### Zatím se jedná pouze o jednoduchý program, ale pokusím se po Vánocích o dodělání tohoto projektu. 

## AKTUÁLNÍ STAV:
#### Pokouším se udělat lepší a větší program na LED pásek, LED pásek v momentální chvíli svítí různýma barvama, bliká a mění intenzitu. Další efekty se pokusím po Vánocích zprovoznit, až na to bude více času.
