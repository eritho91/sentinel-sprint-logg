# Sentinel – Sprintloggbok

**Projekt:** Incidenthanteringssystem  
**Period:** Vecka 47–48, 2026

## Vecka 47 – Projektuppstart

### Fredag 20/11

Idag hade vi vårt första möte kl. 14:15 om applikationen för incidenthantering. Företaget som skolan hade kontakt med hade slutat höra av sig. Jag, Fredrik och Yunus bildade ett Scrum-team och bestämde att jag skulle börja med BE01, Yunus med FE01 och Fredrik med SEC01.

Vi valde arbetsnamnet Sentinel och bokade in vårt första sprintmöte till kl. 13:00 följande måndag. Till en början var vi något osäkra på projektets omfattning, men vi bestämde oss för att påbörja arbetet och reda ut eventuella frågetecken inför nästa möte med Håkan på tisdagen.

Vår initiala förståelse var att vi skulle utveckla en applikation för hantering av IT-incidenter, med möjlighet att använda biometrisk autentisering.

Det första målet var att skapa två fungerande projekt, backend och frontend, med gemensamma arbetsrutiner i Git, automatiserade tester, skyddade main-brancher och en genomtänkt plan för autentisering. På så sätt skulle vi kunna påbörja utvecklingen av incidenthanteringssystemet på ett strukturerat sätt.

### Lördag 21/11

Idag genomförde och slutförde jag BE01.

## Vecka 48 – Sprint 1

### Måndag 23/11

Under helgen slutförde jag BE01 utan några större problem. Jag började även sätta mig in i sessionsbaserad autentisering och WebAuthn inom ramen för SEC01.

På Sprint Planning-mötet bedömde vi att vi skulle hinna genomföra samtliga planerade backlog-items under veckan. Vi estimerade alla items till en story point, med undantag för SEC01 som estimerades till tre story points eftersom uppgiften innefattade en teknisk undersökning.

Därefter fortsatte vi arbeta med våra respektive uppgifter. För min del innebar det BE02 och BE03.

### Tisdag 24/11

Idag slutförde jag de sista kontrollerna för BE04. Vi verifierade att det inte gick att genomföra en merge när en granskningskonversation var olöst. Vi testade även att merge blockerades vid ett misslyckat bygge genom att tillfälligt ändra testet för applikationens start till `assertTrue(false)`. Båda kontrollerna fungerade som förväntat.

Vi hade även ett möte med Håkan där vi bland annat gick igenom SEC01. Jag hade tidigare tänkt att vi skulle kombinera olika tekniker för lösenordshantering och biometrisk autentisering, men insåg att detta kunde innebära större komplexitet än jag först hade räknat med.

På vårt Scrum-möte beslutade vi därför att börja med traditionell lösenordsbaserad autentisering och implementera WebAuthn och biometrisk autentisering vid ett senare tillfälle, när grunden till applikationen börjat ta form.

### Onsdag 25/11

Idag arbetade jag med databasmodelleringen inom DATA01. Jag utgick från en traditionell relationsdatabas eftersom jag än så länge har begränsade kunskaper om grafdatabaser och grafanalys. Det är något vi kan undersöka närmare när vi fått en bättre bild av hur systemet ska fungera.

Jag föreslog separata tabeller för incidenter, organisationer och användare, samt ytterligare tabeller för bland annat ärendehistorik, meddelanden och aviseringar.

Det kommer förmodligen att uppstå problem och nya behov längre fram som gör att vi behöver tänka om kring vissa delar av modellen. Jag ser därför det nuvarande upplägget som en första skiss snarare än en definitiv lösning.

På Daily Scrum gick vi igenom att Fredrik hade genomfört SEC01 och att Yunus hade slutfört FE04. Till torsdagen skulle Fredrik färdigställa dokumentationen för SEC01 och Yunus göra de sista justeringarna i frontend-repot. Jag skulle fortsätta arbeta med DATA01.

### Torsdag 26/11

Idag fortsatte jag arbeta med databasmodellen. Jag upplevde att arbetet var utmanande och insåg att jag behöver utveckla min förmåga att visualisera och modellera system utan att först behöva implementera hela applikationen för att förstå hur delarna hänger ihop.

Jag är van vid att mer eller mindre testa mig fram till lösningar, men förmågan att modellera och planera ett system i förväg är viktig för att spara både tid och energi under utvecklingen.

För punkt 2 i DATA01 tog jag fram ett flödesschema med två kundföretag och två incidenter:

- **Vigil AB:** Ärendet tilldelades en handläggare som åtgärdade problemet och stängde ärendet med en beskrivning av vad som gjordes och hur det gick.
- **Axiom AB:** Ärendet låg kvar i systemet utan ansvarig handläggare.

Jag gick sedan vidare till punkt 3 och undersökte hur vi kan använda tabellen `IncidentHistory` för att spara historiken för ett ärende.

Tanken är att vi ska kunna se vem som har gjort en ändring, när ändringen genomfördes samt vilket värde som fanns före respektive efter ändringen. Modellen kan även användas för andra förändringar än statusändringar, exempelvis ändrad prioritet eller ansvarig handläggare.

### Fredag 27/11

Idag färdigställde vi dokumentationen för SEC01 och gick igenom DATA01 på nytt för att få en bättre förståelse för hur databasmodellen ska fungera i praktiken.

Under Sprint Review kom vi fram till att implementationen av `Notification` och `IncidentHistory` kan vänta, eftersom dessa inte är nödvändiga för att skapa ett grundläggande fungerande flöde från ett skapat till ett avslutat ärende.

Vi beslutade även att fortsätta med den ansvarsfördelning vi haft under veckan:

- **Fredrik:** Autentisering och biometrisk säkerhet.
- **Yunus:** Frontendutveckling.
- **Jag:** Databasutveckling och implementation av databasmodellen.

## Sammanfattning av Sprint 1

Under den första sprinten har vi etablerat den tekniska grunden för Sentinel, arbetat med projektstruktur, automatiserade tester, Git-arbetsflöden, autentiseringsalternativ och databasmodellering.

Vi har även fått en tydligare bild av systemets omfattning och vilka funktioner som behöver prioriteras för att skapa ett första fungerande incidenthanteringsflöde.

Min främsta personliga lärdom under sprinten är vikten av att kunna visualisera och modellera ett system innan implementationen påbörjas. Det är en förmåga jag vill fortsätta utveckla under kommande sprintar.
