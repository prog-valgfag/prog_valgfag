# Test af programmet

Der er mange måder at teste jeres program på. bla kan nævnes:

- Test af funktionalitet : virker det som det skal, er der fejl i koden, er der ting der ikke virker som de skal
- Test af brugervenlighed : er det nemt at bruge, er det intuitivt
- Test af design : er det pænt, er det overskueligt, er det nemt at finde rundt i
- Test af performance : er det hurtigt, er det stabilt, kan det håndtere mange brugere eller store datamængder
- Test af sikkerhed : er det sikkert, er der sårbarheder, kan det modstå angreb

Herudover kan man opdele test i *** brugertest *** eller *** automatiserede-tests ***. 

## Brugertest:
Man får rigtige brugere til at teste programmet og give feedback, mens automatiserede tests er når man skriver kode der tester programmet automatisk, f.eks. unit tests eller integrationstests. Begge dele er vigtige for at sikre at jeres program fungerer som det skal og er brugervenligt.


## Automatiserede tests:

- TestVærktøjer - der kan sumulere brugere f.eks. selenium

- Test-kode  - der tester programmet automatisk, man kan i princippet skrive kode helt uden et framework f.eks. unit tests  

her er et kort eksempel på en unit test i python:

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

