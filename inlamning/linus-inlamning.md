Reflektion - DevOps

Produktens livscykel

Under kursens gång har jag fått en betydligt bättre förståelse om hur en applikation övergår från vanlig kod till en fungerande tjänst. I början tänkte jag inte så mycket på alla steg som behövs efter man har koden klar, men nu har jag förstått hur viktigt det är att hela processen fungerar.

M1 var en mjuk start, komma i gång med github och skapande av repository. M2 kom det fram mera använding av git. Vi börja arbeta med branches, pull requests samt code reviews. Jag lärde mig hur git hjälper till med att hantera ändringar och konflikter, då flera jobbar på samma projekt.

I M3 kom docker fram, docker samt containrar där, hade vi använt tidigare. Hur som helst docker gjorde så vi kan smidigt köra applikationen oberoende av maskin. M4 bestod av tester, alltså hur vi kan kolla att allting fungerar som förväntat. Jag lärde mig dock att tester måste konstant underhållas och utvecklas.

I M5 började det redan se ut som en riktigt DevOps-process. Github Actions gjorde så tester och kontroller kunde köras automatiskt innan merge. I M6 byggdes docker images automatiskt till GHCR och kunde användas utanför vår egna datorer. 

M7 var intressant, då vi manuellt konfigurerade en virtuell server på pouta. Vi lärde oss manuell driftsättning samt att manuellt hantera en server i terminalen. I M8 använde vi Terraform för att beskriva infrastrukturen som kod istället för att skapa allting manuellt. Slutligen M9 som kopplade ihop processen genom att automatisera uppdatering av applikationen i produktion.

Vad går sönder utan automation?

Ett tydligt exempel är skillanden på manuell driftsättning i M7 och automatiserad i M9. I M7 måste vi själva ansluta med SSH till servern, samt utföra stegen som krävdes för att starta applikationen. Det är fungerande, men problemet jag upplevde var att det är väldigt många steg. Man måste komma ihåg alla kommandon samt ordning för använding av dem. Om någon ex. använder fel version av en Docker-image eller vad som helst annat misstag, så kan det leda till att produktionen inte fungerar som förväntat.

Med Automatisering i M9 minskar detta problem eftersom uppdateringen kan utföras på ett förutbestämt sätt då nya ändringar mergas till main. Detta sparar tid och minimerar risken för mänskliga misstag. Automation betyder ändå inte att ingenting kan gå fel. Om ex. själva workflowen är fel konfigurerad så kan samma problem upprepas, vilket betyder att det är viktigt att kontrollera den vid automatisering. Automation för mig i denna miljö handlar om att göra saker snabbare, att skapa en process som är konsekvent och lättare att upprepa, samt minska männskliga misstag.