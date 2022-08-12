# Podstawy js
## Praca w konsoli deweloperskiej 
- aby otworzyć konsolę klikamy ctrl + shift + i lub wchodzimy w więcej narzędzi i narzędzia dla deweloperów
- console.log() - wyświetla informacje w konsoli
- console.error('to jest błąd') - wyświetli błąd w konsoli 
- console.clear(); - wyczyści konsolę 
- console.warn("it's a warning") - wyświetli ostrzeżenie 
...
console.timeEnd(nazwa);

## deklarowanie zmiennych  
- tworzymy przy pomocy: var, let lub const
- var jest starym sposobem od którego się odchodzi
- obecnie najlepiej używać let lub const 
- let pozwala nam na zmianę wartości zmiennej
- wartość const jest stała i nie może być zmieniona 
Przykłady:
```
const greeting = 'Hello world';
let firstName = 'Oliwia';
var age = 10;
```
### nazewnictwo 
Czy możemy nazywać zmienne w dowolny sposób?
Nie, są podstawowe zasady:
- nazwy mogą zawierać litery, cyfry, _, i $
- nie może się zaczynać od cyfry
- jeśli mamy nazwę składającą się z więcej niż jednego słowa, to korzystamy z jednego ze wzorów
```
const firstName = 'John'; // Camel case
const first_name = 'John'; // Underscore
const FirstName = 'simon'; // Pascal case - w niektóych sytuacjach
```
Camel case jest najbardziej polecany 
- w JS wielkość liter ma znaczenie - firstName i FirstName to nie to samo

## typy danych 
### typy prymitywne
 - string
 -Number 
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
### pozostałe operatory porównania
!==, >, < / >=, <=
### operatory logiczne 
- && - operator i - sprawdzamy czy obie zmienne są prawdziwe 
- || - operator lub - sprawdzamy czy chociaż jedna zmienna jest prawdziwa 

## warunki if 
  - if(nasz warunek) {
  - co się stanie, gdy warunek zostanie spełniony
  - }else if (inny warunek) {
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

### Math
- formatowanie - wartość po przecinku

newVal = num1.toFixed(2);
- zaokrąglanie liczb

mathObj = Math.round(2.8);

- zaokrąglanie liczb w górę

mathObj = Math.ceil(2.2)

- zaokrąglanie liczb w dół

mathObj = Math.floor(2.8);

- pierwiastek kwadratowy

mathObj = Math.sqrt(64);

- wartość bezwzględna

mathObj = Math.abs(-100);

- potęgowanie

mathObj = Math.pow(2, 8);

- najmniejsza wartość

mathObj = Math.min(2, 8, 5, 10);

- największa wartość

mathObj = Math.max(2, 8, 5, 10);

- zwraca przypadkową wartość, ale między 0, a 1

mathObj = Math.random();

- jeśli chcemy np randomową wartość do 20, to wystarczy pomnożyć
mathObj = Math.random() * 20;

- konwertwanie na numer

Number('5');

- zmiana na liczbę całkowitą

parseInt('100.544');

- zmiana na liczbę z zachowaniem wartości po przecinku

parseFloat('100.14545453');

Obiekt Math:
https://developer.mozilla.org/pl/docs/Web/JavaScript/Reference/Global_Objects/Math

### Strings
- dodawanie stringów 

 +, += lub concat 
 
- długość stringa

string.length

- zamiana wszystkich liter na wielkie 

string.toUpperCase()
- zamiana wszystkich liter na małe

string.toLowerCase()

- wyciąganie konkretnego znaku 

string[0] lub string.charAt(0)

- wyciąganie kilku znaków z podanych indexów

string.substring(0,4) - zwraca od 0, a 4 litera

lub slice(0,4)
- wyciąganie ostatniego elementu 

string.slice(-1)

- dzielenie stringa 

.split(' ') - zamienia string w tablicę

- wymiana znaków

.replace('słowo/znak do zastąpienia', 'słowo/znak zastępujące')

- sprawdzanie czy dany znak/ciąg znaków znajduje się w stringu
- 
.insludes()

String: 
https://developer.mozilla.org/pl/docs/Web/JavaScript/Reference/Global_Objects/String

### template literals
```
const expression - 'some text'
`string text ${expression} string text`
```
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals


### tablice
- tworzenie tablic

[] lub new Array(1,3)

- długość tablicy 

[1, 2].length

- podmienianie elementów 

arr[1] = 100
- dodawanie elementu na koniec tablicy 

[].push(nowyElement);
- dodawanie elementów na początek 

[].unshift 

- usuwanie elementu z końca

[].pop()

- usuwanie elementu z początku 

[].shift()

- usuwanie kilku elementów
 
[].splice(0, 3)

- wybieranie kilku elementów 

[1, 2, 3].slice(0,1);

- odwracanie kolejności elementów tablicy 

[1, 2, 3, 4].reverse() // otrzymamy [4. 3. 2, 1]

- łączenie tablic

[].concat([1, 2])

### spread operator 
umożliwia kopiowanie elementów z jednej tablicy do drugiej 

```
const tab = [1, 2, 3];
const tab2 = [...tab]
```
### reference types 
przy tworzeniu tablic do zmiennej nie przypisujemy wartości tej tablicy, ale adres do niej, dlatego w takim przypadku:
```
const arr = [1, 2, 3]
const arr2 = arr;
arr2.push(4)
```
wartość 4 zostanie dodana zaróno do tablicy arr2, jak i arr 

Obiekty również należą do reference types 

### obiekty 
obiekty pozwalają nam na przechowywyanie danych w postaci par kluczy i przypisanych do nich wartości np. 
```
const person = {
 firstName: 'Oliwia', 
 age: 23, 
 animals: ['Frania', 'Koda']
}
```

aby otrzymać wartość z danego obiektu używamy kropki, [] lub destrukturyzacji 
```
person.firstName // zwróci Oliwia 
person[age] // zwróci 23
const {animals} = person //destrukturyzajca
```
### destrukturyzacja
dzięki niej możemy wyciągnąć dane z obiektu
- destrukturyzacja obiektu 
```
const {firstName, age, animals} = person
```
-  nadawanie nazw
```
const { firstName: personName, animals: cats } = person;
```
- destrukturyzacja tablicy 
```
const x = [1, 2, 3, 4, 5];
const [y, z] = x; // y = 1, z = 2
const [y, , z] = x // y = 1, z = 3
```
### pętle 
 pętla to instrukcja, która powtarza się dopóki, jakiś określony warunek zostanie spełniony
 - while 
 ```
let i = 0;
while(i< 10) {
 console.log('Number' +i);
 i++
}
```
- do while - zostanie wykonana chociaż raz
```
do {
 console.log('Number'+ i)
 i++
} while(i<10)
```
- for 
```
for (let i =0; i < 10; i++) {
 console.log('Number'+ i)
}
// zmienna i zapamiętuje ile było powtórzeń w pętli
```
- continue - przerywa obecną pętle; pętla przechodzi do następnej iteracji
```
for (let i =0; i < 10; i++) {
 if(i ===2) {
   console.log("numer 2")
   continue
 }
 console.log('Number'+ i);
}
```
- break - całkowicie przerywa pętlę 
```
for (let i =0; i < 10; i++) {
 if(i ===2) {
   console.log("numer 2")
   break; // w tym momencie pętla się przerwie i nie dojdziemy do nr 3 
 }
 console.log('Number'+ i);
}
```
