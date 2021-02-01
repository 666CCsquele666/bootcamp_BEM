# bootcamp_BEM

Opgave:

Lav et markdown (md) dokument på din Github.

Og skriv hvad der tales/beskrives på følgende tidspunkter i videoen:

(emnet startes ved tiden og varer x-antal minutter)

03.50 - 05.20 - 06.30 - 08.57 - 19.05 - 20.50 - 22.06 - 24.20

Og afslutningsvis skal du nu med egne ord skrive lidt om hvad du fik ud af videoen.



1. 03:50 = Decoupling & Single Responsibility Principle:

At adskille objekter, så de bliver mere specifikke. I stedetfor, at have en del "spaghetti-kode" hvor et element eller et objekt dealer med mange forskellige ting, burde mand "decouple" dem, eller udrede dem, så de kun gøre én specifik ting. Det kan godt være at ens kode bliver længere af det, men det bliver tilgengæld også nemmere, at holde styr på de forskellige ting og vide præcist hva denne udredet bid kode gør. 

2. 05:20 = Encapsulation:

I fortsættelsen af, at have decouplet en masse "rodet" kode, har man også et eller andet sted indkapslet de forskellige dele af kodens funktioner. Dvs, at i fremtiden hvis man skal bruge en specifik kode, som gøre en rimelig specifik ting, så har du en bid kode som ikke gøre andet, end netop denne specifikke ting som er koden eneste funktions. 

3. 06:30 = The Media Object:

At skabe et modul som gør nogle af de ting, som du ser gentager sig, på din side, meget mere overskueligt. I denne situtaion har Nicole Sullivan opdaget, at på facebooks side er der nogle af de samme "css principper", som går igen utrolig mange gange. Derfor ville det være smart, at lave et form for genvejs system så det samme kode ikke skulle stå en million gange. Altså lave et såkaldt modul. 

I dette eksempel, navngiver hun hendes modul: "The Media Object" og giver den to børn; et img (.img) og en body (.bd), som hun faktisk har et form for default template og kun selve indholdet skal ændres.

4. 08:57 = SMACSS:

En fyr er kommet med den idé, at opdele al hans CSS-kode i fem kategorier. Så kunne man feks. dele hele sit CSS dokument op i fem dele: 

[Base.css] [Layout.css] [Module.css] [State.css] & den valgfrie [Theme.css]  

Base: Basale HTML elementer. Feks. straight up <HTML>, <BODY>, <H1>, <P> osv osv.
Layout: Store sektioner som et eller andet sted er mere specifikke feks. <HEADER>, <FOOTER>, <SECTION>, <DIV> osv.
Module: Ligesom det module vi snakkede om før (The Medie Object). Altså en form for template, hvor opstillingen af elementer skal gå igen, igen og igen, men hvor det kun er selve indholdet, som skal ændres. 
State: Det omhandler ting, som ændrer tilstand. Elementer som et eller andet sted, ikke er konstante men ændrer sig via Javascript eller anden spændende CSS-magi. Feks. det at "toggle" en class til og fra et element. Altså, den ændrer tilstand (state). 
Theme: Relle hele temaer som skal ændres. Nu til dags er det meget populært feks. at have mulighed for at ændre youtubes udseende til darktheme. Eller hvis det lige har Hannukah og PirateBay ændrer sidens udseende, til at være et Hanukkah tema i Hanukkah ugen. En rimelig specifik og sjælden ting at komme ud for, at være en nødvendighed. 
  
5. 19:05 & 20:50 & 22:06 = SPECIFICITY!!!

Jo mere præcis din CSS-Selektorer er, jo mere 'betydningsfuld' er den og derfor vil den mere specifikke selektore blive vist i stedet for den mindre specifikke. Feks. er "IDs" langt mere specifikke end "Classes". Så feks. [<H1 class="red" id="blue">Specificity</h1>] her vinder ID'en og H1-tagget vil blive blåt i stedetfor rødt. Samtidig er kombineret selektore også mere specifikke. 

Eksempelvis:

    .body h1{
      color: purple;
     }
     
    .ny_farve{
      color: red;
     }
     
<section class="body">
  <h1 class="ny_farve">OVERSKRIFT</h1>
</section>


Her vil "purple" vinde, da det en kombineret selektorer der går ind og vælger "h1" inde i det med classen "body" - fremfor KUN at vælge dem med classen "ny_farve".

8. 24:20 = Flat Selectors:

Sådan som jeg forstår det, er flat selectors meget specifikke single-selectors som reelt kun går ind og styler/ændrer små specifikke ting. Eksemplet som Matt Stauffer bruger i videoen er: [.unordered-list-in-the-body__lidt-item-reversed]. 
Det ser egentligt fuldstændig fucked up ud, men gør det overskueligt på den måde, at den kun har ÉT job. Den går kun ind og rammer det der ene meget specifikke element, begravet i en million andre elementer og ændrer KUN på det.

___________________________________________________________________________________________________________________________________________________________________________

Via videon har jeg lært hvordan jeg kan arrangere min kode på en mere overskuelig måde. Både for mig selv, men også for andre der skal læse min kode. Især i CSS'en. Samtidig med at det bliver mere overskueligt at læse og forstå hvad der rent faktisk gør hvad til hvad, vil det også i fremtiden være nemmere for en, eller for andre, at skulle gå ind og ændre i noget af koden, da selektore bliver meget mere specifikke. 

//Adam CCsquele
