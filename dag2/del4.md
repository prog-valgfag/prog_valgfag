
# 4.del. : Opgave - vareberegner med både akkumuleret pris og vægt !!! - d.13/8-25

-------------------------------------------------------------------
-------------------------------------------------------------------

Vi skal nu lave en ny super vare, pris, vægt beregner. Men husk at bruge jeres viden om hvordan javascript håndterer tal, så i ikke kommer ud for de fejl vi har gennemgået fra tidligere.

![prisOgvaegt](/dag2/PrisOgVaegt.png)

Koden i får denne gang er lidt mere anvanceret nu er der også en "for-løkke" og et "array",- prøv at se om du kan udvide og kopirere de metoder du læser i koden så du på den måde kan færdigøre programmet:

Der er følgende krav til programmet:

- det skal kunne håndtere kommtal og storetal fornuftigt
- alt på interfacet skal stå på en brugerventlig og pæn måde
- din kode skal være letlæslig og så enkel som overhovedet muligt

```javascript
let inputVare 
//let inputPris
//let inputVaegt

//let samletPris;
//let samletVaegt;

let vareList     = [];
//let prisList     = [];
//let vaegtList    = [];

function setup() {
  createCanvas(500,500)
  inputVare     = createInput();
  inputVare.position(70,10);
  //kode mangler
}

function draw(){
  background(255);
  text("vare",10,25); 
  for(let i=0 ; i< vareList.length; i++){
    text(vareList[i] + " ",10,200 + i*20) 
    //kode mangler
  }
}

function keyPressed(){
  if(keyCode != ENTER) return;
  vareList.push(inputVare.value())
  //kode mangler
}

```


