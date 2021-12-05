# Adapter kierownicy MQB
*(doposażenie kierownicy MQB w platformę PQ46 - VW Passat b6/b7, CC)*

Adapter obsługuje przyciski na kółkach (media i tempomat). Pod maską przechwytuje magistralę LIN między jednostką sterującą a przyciskami na kierownicy. Konwertuje kod wciśniętego przycisku z MQB na PQ, akceptowany przez sterownik układu kierowniczego. Zastępuje również dźwignię tempomatu, zamieniając kod wciśniętych przycisków na kierownicy na sygnały dźwigni.

## Jakie wersje sterowników i kół są obsługiwane?
W zasadzie dowolna jednostka sterująca platformy PQ46 obsługująca przyciski na kołach i tempomat. Oraz kierownice platformy MQB, które pasują do zdjęć w katalogu 'firmware'.

Część sprzętowa oparta jest na Arduino Pro Mini (16MHz 5V) i wykorzystuje kilka transoptorów, nadajników LIN i rezystorów pasujących do interfejsu samochodu. Udostępniam pliki Gerber, listę komponentów i instrukcję instalacji.

Oprogramowanie jest prezentowane jako skompilowane pliki oprogramowania układowego. Oprogramowanie układowe różni się w zależności od przycisków sterujących.

## W Planach

* Przebudowa PCB
* Rezygnacja z Arduino
* Zmiana  MCP2003A-E/SN na inny nadajnik
* Naprawa kodu
* Dodanie możliwości Flash'u z poziomu ODIS

## Jak złożyć adapter:
- kup następujące części:
  - Arduino Pro Mini 16MHz 5V
  - 2 transoptory LTV-847S
  - 2 nadajniki LIN MCP2003A-E/SN
  - regulator napięcia 5V L7805CV
  - 2 rezystory 100R w pakiecie 1206 SMD
  - 2 rezystory 150R w pakiecie 1206 SMD
  - 1 rezystor 180R w pakiecie 1206 SMD
  - 3 rezystory 240R w pakiecie 1206 SMD
  - 8 rezystorów 330R w pakiecie 1206 SMD
  - 3 rezystory 390R w pakiecie 1206 SMD
  - 1 rezystor 4K7 w pakiecie 1206 SMD
  - 2-pinowe złącze Dupont 2.54mm (https://www.aliexpress.com/item/32905764355.html)
  - 6-pinowe złącze Edge Card Connector 2,54 Mm Pitch (https://www.aliexpress.com/item/40005773796772.html) - Będziesz musiał wyciąć 6-pinowe złącze, aby pasowało do gniazda jednostki sterującej, Lub możesz pominąć ten element i ponownie użyć złącza z fabrycznej dźwigni tempomatu
- wykonać płytkę PCB na podstawie plików Gerber
- przylutuj wszystko, aby uzyskać ten wynik:

![przód adaptera](https://user-images.githubusercontent.com/5708028/138508025-40673c90-a3f3-4b15-9137-88e356b51d86.jpg)
![tylny adapter](https://user-images.githubusercontent.com/5708028/138508037-250900c1-fe1d-4c1f-a028-7e979f6e01ea.jpg)


## Jak nagrać oprogramowanie:
- najpierw znajdź oprogramowanie układowe pasujące do przycisków na kierownicy. Przejrzyj obrazy w każdym katalogu oprogramowania układowego
- wgraj firmware do Arduino za pomocą dowolnego dostępnego programatora


### Postępuj zgodnie z instrukcją, aby zainstalować adapter w samochodzie:
https://github.com/v-ivanyshyn/mqb-steering-wheel-adapter/blob/main/Manual%20EN.pdf
