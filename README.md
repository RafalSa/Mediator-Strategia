1. Kiedy istnieje konieczność zarządzania zasobami za pomocą metody Dispose()? 
Czy metodę Dispose() można przeciążać? Jeśli tak to w jakim celu?

Dispose() jest potrzebne, gdy Twoja klasa "trzyma" jakieś zasoby spoza .NET, np. plik, i trzeba je ręcznie zwolnić, a przeciążenie Dispose(bool) to technika, by zrobić to sprzątanie bardziej elastycznie (np. inaczej przy ręcznym wywołaniu, inaczej przy sprzątaniu przez system).

2. Wyjaśnij czy oba poniższe programy z punktu a) oraz b) są poprawne? Krótko 
uzasadnij.

Program 'a' jest poprawny i bezpieczny dzięki IDisposable i using, które samo pilnuje zamknięcia pliku, za to program 'b' jakoś działa, ale jest ryzykowny, bo wymaga ręcznego pamiętania o zamknięciu.


## a)

*![Header](https://github.com/RafalSa/Mediator-Strategia/blob/master/Zrzut%20ekranu_27-4-2025_151818_.jpeg)*

## b)

*![Header](https://github.com/RafalSa/Mediator-Strategia/blob/master/Zrzut%20ekranu_27-4-2025_15182_.jpeg)*
