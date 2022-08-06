# js-podstawy

## Praca w konsoli deweloperskiej 
- aby otworzyć konsolę klikamy ctrl + shift + i lub wchodzimy w więcej narzędzi i narzędzia dla deweloperó 
- console.log() - wyświetla informacje w konsoli
- console.error('to jest błąd') - wyświetli błąd w konsoli 
- console.clear(); - wyczyści konsolę 
- console.warn("it's a warning") - wyświetli ostrzeżenie 
- console.time(nazwa); - zwróci nam czas jaki był potrzebny do wykonania zadań między time i timeEnd
...
console.timeEnd(nazwa);

## deklaroawnie zmiennych  
- tworzymy przy pomocy: var, let lub const
- var jest startm sposobem od któego się odchodzi
- obecnie najlepiej używać let lub const 
- let pozwala nam na zmianę wartości zmiennej
- wartość const jest stała i nie może być zmieniona 
Przykłady:
const greeting = 'Hello world';
let firstName = 'Oliwia';
var age = 10;

### nazwenictwo 
Czy możemy nazywać zmienne w dowolny sposób?
Nie, są podstawowe zasady:
- nazwy mogą zawierać litery, cyfry, _, i $
- nie może się zaczynać od cyfry
- jeśli mamy nazwę składającą się z więcej niż jednego słowa, to korzystamy z jednego ze wzorów
const firstName = 'John'; // Camel case
const first_name = 'John'; // Underscore
const FirstName = 'simon'; // Pascal case - w niektóych sytuacjach
Camel case jest najbardziej polecany 
- w JS wielkość liter ma znaczenie - firstName i FirstName to nie to samo

## typy danych 
### typy prymitywne
 - string
  - Number //(nie ma różnicy między int, float itp)
 - Boolean
 - null
 - undefined
 - symbol (ES6)

### typy złożone
 - obiekty:
   - tablice
   - funkcje
   - Date // daty
   - itp.
### typowanie dynamiczne
 typy są powiązane z wartością zmiennej, a nie samą zmienną
 zmienne mogą przyjmować różne wartości - najpierw może być string, a później np numer
  
 typeof lub type of zmienna- pozwala nam sprawdzić jaki jest typ zmiennej 
 typeof null to obiekt - to jest błąd js

## porównywanie
### operator równości 
== - pozwala nam porównać wartości zmiennych  
=== - strict equality - porónuje zarówno wartość zmiennej, jak i jej typ 
np. '2' == 2 zwróci true
2 === '2' zwróci false 
### pozostałe operatory porónania
!==, >, < / >=, <=
### operatory logiczne 
- && - operator i - sprawdzamy czy obie zmienne są prawdziwe 
- || - operator lub - sprawdzamy czy chociaż jedna zmienna jest prawdziwa 

## warunki if 
  - if(nasz warunek) {
  - co się stanie =, gdy warunek zostanie spełniony
  - }else if (iiny warunek) {
  - co się stanie, gdy inny warunek zostanie spełniony 
  - } else {
  - co jeśli żaden ze wcześniejszych warunków nie jest spełniony 
  }

### wartości falsy: - wartości, które zwrócą nam false w if
- false
- null 
- undefined 
- '' - pusty string 
- 0 
= NaN 

### wartości truthy:
- true 
- string (który nie jest pusty)
- numer (inny niż zero)
- tablica (może być nawet pusta)
- obiekty 
- itp

Obiekt Math:
https://developer.mozilla.org/pl/docs/Web/JavaScript/Reference/Global_Objects/Math

String: 
https://developer.mozilla.org/pl/docs/Web/JavaScript/Reference/Global_Objects/String
