# Suplerende stof : Supabase,- relationel database og webservice

## introduktion til supabase - del 19.1

supabase er en open source backend som en service platform der gør det nemt at lave databaser til web og mobil apps.

Nye ting at lære her:
- en webservice
- relationel database (postgres)
- sql


## Hvad er en relationel database?
En relationel database er en type database der organiserer data i tabeller som kan relateres til hinanden gennem nøgler. Hver tabel består af rækker og kolonner.

Gode fordele ved relationelle databaser:
- Struktureret data : Data organiseres i tabeller med definerede skema
- Relationer : Tabeller kan relateres til hinanden gennem nøgler, hvilket muliggør komplekse forespørgsler og datahåndtering.
- SQL : Structured Query Language (SQL) bruges til at manipulere og forespørge data, hvilket er et kraftfuldt og standardiseret sprog.
- Dataintegritet : Relationelle databaser understøtter dataintegritet gennem constraints, som sikrer at data

Gode regler for design af relationelle databaser:
- Normalisering : Organiser data for at minimere redundans og afhængigheder.
- Primærnøgler : Hver tabel bør have en primærnøgle der entydigt identificerer hver række.
- Fremmednøgler : Brug fremmednøgler til at etablere relationer mellem tabeller.

## [HER : et eksempel på p5js kode der forbinder til supabase og henter data fra en tabel kaldet "dyr":](/dag19/del19_2_eksempel.md)

