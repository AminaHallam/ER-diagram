# ER-diagram
Designa två stycken ER-diagram baserat på ett specifik case. Utöver dessa diagrammen skall en halv sida innehållande en enkel beskrivning av diagrammets uppbyggnad medfölja inlämningen. Här är det bra att lyfta fram de mer komplexa delar av diagrammen samt kort motivera hur dessa hänger ihop.


ER-diagram 1

Det första diagrammet skall vara konceptuellt och holistiskt samt vara utformat för en projektledare/kund. Utöver de entiteter, relationer och attribut som finns med i caset (på sida 3) skall minst en av varje av följande finnas med i det första diagrammet:

Ett multipelt attribut
Ett härlett attribut
Ett sammansatt attribut
Ett fullständigt deltagande
Ett flervägssamband

Båda diagrammen skall innehålla kardinaliteter.

Gamingsoft: Multi User Dungeon Game

 

Det finns en klass av dataspel som kallas massively multiplayer online role-playing games, eller MMORPG. Det är spel där man spelar en rollfigur, till exempel en riddare, som går runt i en simulerad värld och slåss med monster, samlar skatter eller bara pratar med andra spelare som spelar samma spel och går runt i samma simulerade värld. Ett par kända såna spel är EverQuest och World of Warcraft.

Redan på sjuttiotalet fanns det textbaserade liknande spel, där man (precis som i de moderna MMORPG-spelen) spelar en rollfigur, går runt i en simulerad värld, och interagerar med andra spelare. En klass av såna textbaserade spel kallas Multi-user dungeon, eller MUD. Man styrde sin rollfigur med kommandon som "gå norrut", "ta upp väskan" och "anfall björnen".

I den här uppgiften ska vi skapa en databas som kan användas för lagring av data i ett MUD.

 

De saker som ska lagras i databasen är följande:

 

1 Spelare. En "spelare" är egentligen inte en representation av själva spelaren, utan av den rollfigur som spelaren spelar i spelet. Spelaren (dvs rollfiguren) har ett unikt namn, en (inte nödvändigtvis unik) beskrivning, och några "stats", dvs värden som beskriver rollfigurens egenskaper: styrka, skicklighet, friskhet och hur många poäng som spelaren samlat ihop. Spelarna måste finnas kvar i databasen även när de loggar ut. En spelare som dör i spelet försvinner inte, utan förlorar bara sina saker och en del av sina poäng.

 

2 Monster. Ett "monster" behöver inte vara grönt och ha många tänder, utan alla figurer i spelet som styrs av datorn och inte av en spelare kallas för monster. Ett monster har, precis som en spelare, ett namn, en beskrivning och dessutom samma "stats" som spelarna. En skillnad är att namnet inte behöver vara unikt, utan det kan till exempel finnas många grodor som allihop heter Groda. Ett monster som dör i spelet försvinner.

 

3 Rum eller platser. Det här är de platser som spelarna och monstren kan gå omkring i. Varje spelare som är inloggad i spelet befinner sig i ett visst rum. Spelare som inte är inloggade, befinner sig inte i något rum. En del rum kan vara tomma. Varje rum har ett unikt nummer, ett (inte nödvändigtvis unikt) namn och en (inte nödvändigtvis unik) beskrivning.

 

4 Saker. Det här är de saker som finns i spelet, förutom rum, spelare och monster. Det kan till exempel vara stenar, guldmynt, svärd och tulpaner. Sakerna kan ligga och skräpa i rummen, och dessutom kan både spelarna och monstren plocka upp sakerna och bära omkring på dem. Varje sak befinner sig antingen i ett visst rum, eller på en viss spelare eller monster. Varje sak har ett (inte nödvändigtvis unikt) namn och en (inte nödvändigtvis unik) beskrivning.


5 Servrar. Spelvärlden är så stor att den inte kan hanteras av en enda dator, utan den är uppdelad på ett antal olika datorer, eller servrar. Varje rum hör till en viss server. Spelarna och monstren kan däremot flytta sig mellan servrarna. Varje server har ett IP-nummer (dvs dess Internet-adress), som kan ändras ibland men som är unikt vid varje tillfälle.

De flesta mudden var ganska små, och kördes på en enda server. De innehöll kanske tio tusen rum eller platser, och några tiotal samtidiga spelare. Men nu tänker vi oss att vi ska konkurrera med EverQuest och World of Warcraft, så vi vill kunna hantera hundratalas servrar, miljoner rum, och tiotusentals spelare.