# Owczarnia parametryczna

Interaktywne narzędzie opracowane jako część pracy magisterskiej:

**„Zastosowanie systemów wieloagentowych w optymalizacji złożonych układów funkcjonalnych. Projekt centrum przetwórstwa wełny i hodowli w Starym Bożejewie.”**

**Autor:** Magdalena Justyna Barcicka  
**Wydział Architektury Politechniki Warszawskiej, 2026**

Strona jest cyfrowym uzupełnieniem części badawczej i projektowej pracy. Pozwala
samodzielnie zmieniać parametry układu, obserwować działanie symulacji agentowej
oraz przeglądać warianty analizowane w skali budynku i osadnictwa.

**Wersja online:**  
https://<nazwa-uzytkownika>.github.io/<nazwa-repozytorium>/

## Co można zobaczyć na stronie

### Arkusz 01: Owczarnia i symulacja

Pierwszy arkusz przedstawia parametryczny model budynku hodowlanego i hali
strzyżenia. Pięć parametrów P001-P005 pozwala zmieniać wymiary wybranych stref
oraz głębokość hali. Wraz ze zmianą parametrów aktualizują się geometria rzutu,
liczba stanowisk strzyżenia i pojemność układu.

Na rzucie działa również symulacja agentowa. Owce są reprezentowane jako
niezależni agenci przemieszczający się przez kolejne zagrody, bramy i stanowiska
strzyżenia. Po strzyżeniu kierowane są w stronę wyjścia.

Kursor lub dotyk ekranu może pełnić funkcję zaganiacza i wpływać na kierunek
ruchu stada.

Dodatkowe narzędzia pozwalają porównywać warianty za pomocą rankingu, frontu
Pareto i modelu zastępczego. Dostępne są również mapa zagęszczeń, ślady
trajektorii oraz eksport wyników do CSV.

### Arkusz 02: Skala osadnicza

Drugi arkusz pokazuje analizę projektu w szerszej skali.

Lokalny wzorzec zabudowy wyznaczono na podstawie 25 istniejących siedlisk
z okolicy Starego Bożejewa. Każde z nich opisano za pomocą 14 cech
morfologicznych.

Warianty nowej lokalizacji oraz rozbudowy istniejącego gospodarstwa są
porównywane z lokalnym wzorcem przy użyciu odległości Mahalanobisa. Przed
utworzeniem rankingu sprawdzane są również twarde ograniczenia przestrzenne.

Mapa pozwala przełączać widok istniejących siedlisk, wszystkich wygenerowanych
kandydatów oraz wariantów, które przeszły ocenę. Można również wskazać własną
lokalizację i sprawdzić jej wynik według tej samej metody.

## Jak należy interpretować wyniki

Narzędzie zostało przygotowane przede wszystkim do porównywania wariantów
projektowych.

Symulacja agentowa nie jest modelem rzeczywistego stada skalibrowanym na
podstawie pomiarów w istniejącym obiekcie. Parametry zachowania owiec przyjęto
na podstawie literatury, dlatego wyniki służą przede wszystkim do obserwowania
różnic pomiędzy układami i identyfikowania potencjalnych problemów przepływu.

Model zastępczy wykorzystuje pomocniczy wskaźnik wydajności symulacyjnej
mierzony w stałym budżecie czasu. Nie należy go interpretować jako rzeczywistej
przepustowości hali.

Analiza osadnicza opisuje podobieństwo morfologiczne wariantów do lokalnego
wzorca zabudowy. Nie zastępuje analizy planistycznej ani decyzji projektowej.

## Informacje techniczne

Publiczna wersja strony znajduje się w pliku `docs/index.html`.

Jest to samowystarczalna strona statyczna. Geometria, dane oraz kod wykonywany
w przeglądarce są zapisane w jednym pliku i do działania nie jest potrzebny
zewnętrzny serwer ani baza danych.

Na mniejszych ekranach układ dostosowuje się do dostępnej szerokości. Na
telefonie wyświetlany jest przede wszystkim rzut, na którym działa symulacja.
Sterowanie zaganiaczem obsługuje zarówno mysz, jak i ekran dotykowy.

Plik `docs/index.html` jest generowany automatycznie na podstawie wersji
roboczej narzędzia i nie powinien być edytowany ręcznie.

## Publikacja

Strona jest publikowana za pomocą GitHub Pages z katalogu `docs` na gałęzi
`main`.
