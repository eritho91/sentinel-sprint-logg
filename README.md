# sentinel-sprint-logg

Sentinel - Sprint Loggbok

# v48 - SPRINT 1
## Onsdag 25/11
Idag jobbade jag med databasmodelleringen. Jag utgick från en vanlig relationsdatabas eftersom jag än så länge kan för lite om grafdatabaser och grafanalys. Det kan vi kika närmare på när vi fått en bättre bild av hur systemet ska fungera.
Jag tänkte mig separata tabeller för incidenter, organisationer och användare, samt ytterligare tabeller för bland annat ärendehistorik, meddelanden och aviseringar.
Det kommer förmodligen att dyka upp problem och nya behov längre fram som gör att vi behöver tänka om kring vissa delar av modellen. Jag ser därför det nuvarande upplägget som en första skiss och inte som något som är hugget i sten.

## Tisdag 24/11
Idag gjorde jag klart de sista kontrollerna för BE04. Vi testade att det inte gick att merga utan löst granskningskonversation, vilket funkade, sedan även att det inte går att merga om bygget misslyckas (genom att ändra testet för applikationens start till assertTrue(false)).

Vi hade möte med Håkan och gick igenom SEC01, bl.a. Jag trodde man kunde kombinera olika tekniker för lösenordshantering och biometrik men det var, som jag uppfattade det, svårt. Därför bestämde vi på scrum mötet att vi börjar med vanligt lösenord och implementerar biometrik och WebAuthn vid ett senare tillfälle när grunden till appen börjat ta form.

## Måndag 23/11
Över helgen gjorde jag BE01 utan problem. Jag började även lära mig mer om skillnaden mellan SessionStorage och WebAuthn (SEC01). På Sprint Planning-mötet kom vi fram till att vi hinner med alla items i backloggen den här veckan med råge. Vi estimerade alla items till 1 poäng utom SEC01 som blev en 3:a, då det gällde en undersökning, sedan fortsatte vi jobba med våra respektive items; Jag med BE02 och BE03.

# v47
## Fredag 20/11
Idag hade vi första mötet kl 14:15 om appen för incidenthantering. Företaget som skolan hade kontakt med hade slutat höra av sig. Jag, Fredrik och Yunus hamnade i ett sprint team, och vi bestämde att jag börjar med BE01, Yunus med FE01 och Fredrik med SEC01. Vi valde arbetsnamnet Sentinel och valde kl 13:00 följande måndag som första sprintmöte. Vi förstod inte riktigt vad vi skulle göra först men att vi börjar och ser om det skulle klarna inför nästa möte med Håkan följande tisdag. 

Vad vi faktiskt snappade upp var att vi skulle göra en app som hanterar diverse systemfel, och den ska helst använda biometrik som säkerhet. Första målet var att få två fungerande projekt (backend och frontend) med gemensam git-struktur, automatiserade tester, skyddade mainbrancher och en genomtänkt plan för autentisering. Allt skulle vara förberett så att vi sedan kunde börja utveckla incidenthanteringssystemet på ett strukturerat sätt. 

## Lördag 21/11
Idag gjorde jag BE01


ø
