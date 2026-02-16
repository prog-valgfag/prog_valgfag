# Suplerende stof : Supabase,- relationel database og webservice

## introduktion til supabase - del 19.1

supabase er en open source backend som en service platform der gør det nemt at lave databaser til web og mobil apps.

Her er en simpel p5js-applikation, der forbinder til supabase og henter data fra en tabel kaldet "dyr":

### 1 - Først opretter du en supabase bruger, - et projekt og table.

Husk at disable RLS (Row Level Security) for tabellen "dyr" for at kunne hente data uden at skulle håndtere autentificering i dette eksempel.

![](/dag19/pic_sbase_rls_disabled.png)

#### Her ses project ID

![](/dag19/pic_sbase_projectID.png)

#### Her ses API key

![](/dag19/pic_sbase_apikey.png)


### 2 - Så installerer du supabase biblioteket i dit p5js projekt.

![](/dag19/pic_sbase_index.png)

### 3 - Du kan nu anvende supabase i din p5js kode for at hente data fra din "dyr" tabel.

![](/dag19/pic_sbase_script.png)
