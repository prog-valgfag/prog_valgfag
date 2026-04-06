# Test af programmet

Der er mange måder at teste jeres program på. bla kan nævnes:

---------

## Test områder:

- TEST AF FUNKTIONALITET : virker det som det skal, er der fejl i koden, er der ting der ikke virker som de skal
- TEST AF BRUGERVENLIGHED : er det nemt at bruge, er det intuitivt
- TEST AF DESIGN : er det pænt, er det overskueligt, er det nemt at finde rundt i
- TEST AF PERFORMANCE : er det hurtigt, er det stabilt, kan det håndtere mange brugere eller store datamængder
- TEST AF SIKKERHED : er det sikkert, er der sårbarheder, kan det modstå angreb

Selve testningen kan foregå enten som ***brugertest*** eller ***automatiserede tests***

-------------------

## Brugertest:
Dette er når man får rigtige brugere til at teste programmet. Det er vigtigt at få feedback fra rigtige brugere, da de ofte kan finde fejl og mangler som man selv ikke har tænkt på. Men det er også vigtigt at overveje hvordan og hvem man får til at teste. Der er megen vigtig teori omkring hvordan man udfører brugertest.  
Overvej som minimum følgende spørgsmål:

- Er testeren objektiv? ( f.eks. er det en ven der har hjulpet med at lave programmet, så er det måske ikke den bedste tester )
- Er testeren i målgruppen for programmet? ( f.eks. hvis det er et program der skal bruges af børn, så er det måske ikke den bedste tester at få en voksen til at teste )
- Ved testeren hvad de skal teste? ( måske er det en god idé at lave en testplan, så testeren ved hvad de skal teste og hvordan de skal teste )
- Skal der måles eller observeres noget under testen? ( f.eks. hvor lang tid det tager at udføre en opgave, hvor mange fejl der laves, hvordan testeren reagerer på forskellige ting )
- Skal der laves flere runder af test? ( for at kunne sige noget mere statistisk om testresultaterne, så er det en god idé at lave flere)

## Automatiserede tests:

- TEST VÆRKTØJ - der kan sumulere brugere f.eks. selenium 

[https://www.selenium.dev/selenium-ide/](https://www.selenium.dev/selenium-ide/)

- TEST KODE  - der tester programmet automatisk, man kan i princippet skrive kode helt uden et framework f.eks. unit tests  

her er et kort eksempel på en unit test i javascript, der tester en simpel add funktion:

```javascript
// 1. Funktionen der skal testes
function add(a, b) {
  return a + b;
}

// 2. Selve testen
function testAdd() {
  const result = add(2, 3);
  const expected = 5;

  if (result === expected) {
    console.log("✅ Testen bestod!");
  } else {
    console.error(`❌ Testen fejlede! Forventede ${expected}, men fik ${result}`);
  }
}

// Koer testen
testAdd();
```


------------------------------------------------------------------------------------------------

## Hvilke typer test skal I lave?

Det er langt fra sikkert at alle typer test er relevante for jeres projekt, det kommer helt an på hvad det er for et program I laver. Det vigtigste er at I tester jeres program grundigt og dokumenterer det i synopsen. Det er en god idé at lave både brugertest og automatiserede tests, så I får både feedback fra rigtige brugere og sikrer at jeres program fungerer som det skal.