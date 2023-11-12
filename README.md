
### Webbaserat Spel: Skapa och Strida med Karaktärer

#### Projektöversikt

I detta projekt kommer vi att skapa ett enkelt webbaserat spel där spelare kan:

1. Skapa spelkaraktärer med hjälp av ett formulär.
2. Spara dessa karaktärer i en lista.
3. Välja två karaktärer från listan och låta dem delta i en strid.

#### Steg 1: Skapa Spelkaraktärer som Objekt

**Vad är ett Objekt?**
Ett objekt i JavaScript är en samling av relaterade data och funktioner. Dessa data kallas egenskaper, och varje egenskap har ett namn och ett värde. 

**Skapa ett Objekt med en Konstruktor**
Vi börjar med att definiera en konstruktor som skapar ett karaktärsobjekt med egenskaper som namn, styrka, intelligens, m.m.

```javascript
function Karaktar(namn, styrka, intelligens, hälsa, speed, attack, hp) {
  this.namn = namn;
  this.styrka = styrka;
  this.intelligens = intelligens;
  this.hälsa = hälsa;
  this.speed = speed;
  this.attack = attack;
  this.hp = hp;
}

// Exempel på att skapa en karaktär
const trollkarlen = new Karaktar("Gandalf", 7, 15, 10, 6, 5, 100);
```

#### Steg 2: Samla Karaktärer i en Array

**Vad är en Array?**
En array är en lista där vi kan lagra flera värden. I vårt fall kommer vi att använda en array för att lagra karaktärsobjekt.

**Skapa och Använda en Array**
Vi skapar en array och lägger till våra karaktärer i den.

```javascript
let karaktarLista = [];
karaktarLista.push(trollkarlen);

const krigaren = new Karaktar("Aragorn", 10, 7, 12, 8, 10, 120);
karaktarLista.push(krigaren);
```

#### Steg 3: Genomföra Strider Mellan Karaktärer

**Genomföra en Strid**
Vi använder en funktion för att simulera en strid mellan två karaktärer. Striden avgörs av egenskaperna `hp`, `attack` och `speed`.

```javascript
function strid(karaktar1, karaktar2) {
  // ...stridslogik...
}

// Genomför en strid
const vinnare = strid(karaktarLista[0], karaktarLista[1]);
console.log(vinnare.namn + " vann striden!");
```

#### Ytterligare Steg för Projektet

- **Skapa ett Användargränssnitt:** Ett webbformulär för att låta spelaren skapa nya karaktärer.
- **Visa Karaktärslistan:** Ett sätt att visa alla skapade karaktärer på webbsidan.
- **Interaktiva Strider:** Möjlighet för spelaren att välja vilka karaktärer som ska strida.

Denna översikt och kodexempel ger en grundläggande förståelse för att skapa och hantera objekt och arrayer i JavaScript, samt hur man använder dessa för att bygga enkla men interaktiva webbapplikationer.
