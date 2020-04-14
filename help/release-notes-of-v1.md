---
title: Opmerkingen bij de release van de AEM-bureaubladtoepassing voor versie 1.x
description: Geef details, verbeteringen, nieuwe functies, compatibiliteit en downloadkoppelingen op voor AEM-bureaubladtoepassing versie 1.x.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f69ccbf7acaa277a7f4d07fabba2094459e4ea23

---


# Opmerkingen bij de release AEM-bureaubladtoepassing v1.x{#aem-desktop-app-release-notes}

Voor desktop app v1.x release zijn de volgende downloadkoppelingen en compatibiliteitsinformatie over AEM.

| Producten | Adobe Experience Manager (AEM)-bureaubladtoepassing |
|---------------|--------------------------------------------------------------------|
| Versie | 1.10 (1.10.0.6 op Mac en 1.10.0.3 op Windows) |
| Type | Minder release |
| Date | 1.10.0.6 (Mac): 15 april 2020; 1.10.0.3 (Win): 31 augustus 2018 |
| URL&#39;s downloaden | [Mac OS X 64-bits](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-1.10.0.6.dmg); [Windows 32-bits](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-1.10.0.3.exe); [Windows 64-bits](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-1.10.0.3.exe) |
| Compatibiliteit | AEM 6.5.x; AEM 6.4.x; AEM 6.3 SP2; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |

>[!NOTE]
>
>Limiet voor cachegrootte wordt niet afgedwongen. Wanneer de bureaubladtoepassing wordt gestart, wordt de cachegrootte eenmaal berekend en wordt een melding weergegeven als de grootte dicht bij de vooraf gedefinieerde limiet ligt.

## Systeemvereisten en -vereisten {#system-requirements-and-prerequisites}

AEM Desktop is compatibel met de volgende besturingssystemen:

* Mac OS X 10.10 of hoger, met de meest recente opgeloste problemen.
* Vensters 7 en Vensters 10 met de recentste de dienstpakken en insectenmoeilijke situaties.

Adobe raadt u ten zeerste aan de nieuwste versie van de AEM-bureaubladtoepassing te gebruiken voor de nieuwste functionaliteit, de meest recente opgeloste problemen en de beste prestaties.

De versie van de AEM-bureaubladtoepassing die u op uw lokale computer wilt installeren, vereist een specifieke AEM-serverversie/aanvullende serveronderdelen (servicepakketten, hotfixes of functiepakketten). Zorg ervoor dat de AEM-server correct is geconfigureerd voordat u er voor het eerst verbinding mee maakt. Neem contact op met de AEM-beheerder als u hulp nodig hebt.

Zie de [gedetailleerde verenigbaarheidsmatrijs](#compatibilitymatrix) aan het eind van dit document om de eerste vereisten voor uw opstelling te evalueren.

## Nieuw in AEM-bureaubladtoepassing 1.10 {#what-s-new-in-aem-desktop-app}

De AEM-bureaubladtoepassing 1.10 richt zich op het verbeteren van de gebruikerservaring bij grote uploads, informatie over de achtergrondbewerkingen en geoptimaliseerde ervaring bij het openen van elementen met gekoppelde bestanden (zoals InDesign).

>[!NOTE]
>
>Gebruik ten minste versie 1.10.0.6 van de app als u MacOS 10.15.4 of hoger gebruikt. Deze patchrelease voldoet aan de notariatievereisten [van](https://developer.apple.com/news/?id=04102019a)Apple.

**Lokaal bewerken/uitchecken**: Automatisch uploaden van wijzigingen die zijn opgeslagen naar elementen kan worden uitgeschakeld in het statusvenster. Op die manier kan de gebruiker aan bestanden blijven werken en wijzigingen opslaan en vervolgens, wanneer deze gereed zijn, besluiten alle wijzigingen te uploaden.

**Venster** Vereenvoudigd middelenstatus: Het statusvenster is vereenvoudigd * Het tabblad Uploads bevat nu zowel afzonderlijke elementen als mappen/bulkuploads. Het vorige tabblad Bulk-uploads is verwijderd.

**Pictogram van toepassing om bulkuploads** aan te geven: Het toepassingspictogram geeft aan dat een bulkupload wordt uitgevoerd door een &quot;transfer&quot;-overlay weer te geven.

**Meldingen voor conflicten** bijwerken: Wanneer de toepassing een conflict ontdekt wanneer het proberen om activa bij te werken, zal het een bericht tonen, zodat de gebruiker dat kan herzien zonder de behoefte om het statusvenster te controleren. Wanneer de toepassing wordt gestart, wordt gecontroleerd op alle conflicten, zodat de gebruiker deze kan oplossen.

**Betere afhandeling van verbindingsverliezen**: Bulkuploads worden gepauzeerd als er een verbindingsverlies is, en de gebruiker zal later kunnen hervatten. Er is een knop Opnieuw proberen beschikbaar om een mislukte upload van een afzonderlijk bestand opnieuw te proberen.

## Installatie-instructies {#installation-instructions}

Zie AEM-bureaubladtoepassing [](install-configure-app-v1.md)installeren en configureren voor gedetailleerde instructies.

## Verbeteringen in de vorige versies {#enhancements-in-the-previous-versions}

Deze release breidt de vorige versies van de Experience Manager-bureaubladtoepassing uit en vervangt deze. Deze versie biedt de volgende belangrijke verbeteringen:

* **Versie 1.9/1.9.1**: herbruikbare uploads, verbeterd statusvenster, toepassingspictogrammen die de status van de toepassing/verbinding aangeven, vooraf ophalen van gekoppelde elementen voor InDesign-bestanden
* **Versie 1.8**: betere controle van geheim voorgeheugengrootte voor de gebruiker, betere login ervaring voor SAML/SSO op Vensters, ondersteunend .pac netwerkvolmacht op MAC, en klant-gemelde kwesties.
* **Versie 1.7**: verbeteringen in stabiliteit en caching logica, betere steun voor netwerkvolmacht, en capaciteit om interne dossiers na uninstallation schoon te maken.
* **Versie 1.6**: verbeteringen in het aanmeldingsproces voor verschillende AEM-beveiligingsconfiguraties en de stabiliteit en prestaties van de toepassing.
* **Versie 1.5**: stabiliteit en veerkracht van de toepassing tegen diverse voorzien van een netwerkproblemen, betere steunbaarheid.
* **Versie 1.4**: de mogelijkheid om hiërarchische mappen op de achtergrond te uploaden met voortgangscontrole.
* **Versie 1.3**: prestatieverbeteringen en stabiliteit bij het openen van bestanden en het opslaan van wijzigingen in AEM, met name vanuit Creative Cloud-bureaubladtoepassingen zoals InDesign, Illustrator of Photoshop. Het was bedoeld om gebruikers een meer lokale desktop-achtige ervaring te bieden wanneer het werken met dossiers, terwijl tegelijkertijd de verrichtingen van de netwerkgegevensoverdracht op de achtergrond behandelen.

### Verbeteringen beschikbaar sinds AEM-bureaubladtoepassing 1.9 {#Enhancements-Available-Since-AEM-Desktop-App-19x}

Adobe Experience Manager (AEM) desktop app 1.9.1 was een patchrelease waarmee een aantal belangrijke problemen van klanten met betrekking tot het uitchecken van bedrijfsmiddelen en het kopiëren van bestanden van gedeelde netwerken naar een lokale map werden opgelost.

* Activa die door een gebruiker zijn uitgecheckt, mogen niet voor andere gebruikers beschikbaar zijn (CQ-4246009)
* Kopie van toegewezen map naar een lokale map ondersteunen wanneer de gebruikersmap zich op een aparte schijfpartitie bevindt (CQ-4243978)

De AEM-bureaubladtoepassing 1.9 was gericht op het verbeteren van de gebruikerservaring bij grote uploads, informatie over de achtergrondbewerkingen en geoptimaliseerde ervaring bij het openen van elementen met gekoppelde bestanden (zoals InDesign).

**Herbruikbare uploads**Voor uploads, vooral rond grote dossiers, is er een optie om hen in het nieuwe venster van de Status van Activa te pauzeren/te hervatten.
**Verbeterd venster**voor de status van het element Een verbeterd venster voor de status van het element bevat informatie over de volgende elementen:
Wijzigingen

* Hiermee worden wijzigingen in de wachtrij weergegeven
* Toont uploads in uitvoering, met inbegrip van een vooruitgangsbar, overdrachtssnelheid, totale dossiergrootte, en grootte die tot nu toe worden overgebracht
* Voltooide uploads weergegeven met totaal overgedragen en eindsnelheid
* De weergave van geüploade bestanden is mislukt, samen met een foutbericht en overdrachtgegevens, indien beschikbaar
* Uploads die drie keer zijn mislukt, geven een foutbericht weer
* Conflicterende bestanden die worden weergegeven met een pictogram waarop de gebruiker kan klikken. Klik op het pictogram om een dialoogvenster met een uitleg en twee opties weer te geven:
   * &quot;Mijn houden&quot;: uploadt het bestand onmiddellijk naar de server
   * &quot;Mijnoverschrijven&quot;: verwijdert het lokale bestand onmiddellijk en downloadt een nieuwe kopie van de server

Downloads

* Hier worden downloads tijdens de uitvoering weergegeven, inclusief een overdrachtsnelheid en de grootte die tot nu toe zijn overgedragen
* Voltooide downloads weergegeven met het totaal overgedragen geheugen, de eindsnelheid en een pictogram waarmee het bestand wordt geopend wanneer erop wordt geklikt (alleen beschikbaar voor afzonderlijke bestanden)
* Mislukte downloads weergegeven met een foutbericht en overdrachtsinformatie, indien beschikbaar
* In de voettekst ziet u het totale aantal gedownloade bestanden en de gemiddelde overdrachtsnelheid.
* Als een gebruiker ervoor kiest om meerdere bestanden te openen of bewerken via de interface van het AEM Assets-web, worden deze samen gegroepeerd, bijvoorbeeld &quot;mijnelement.jpeg en vier andere bestanden&quot;
* Wanneer u InDesign-documenten downloadt, inclusief gekoppelde elementen die zijn opgeslagen in AEM Assets, downloadt de bureaubladtoepassing eerst alle gekoppelde elementen voordat u het InDesign-document opent en geeft de download van gekoppelde elementen bijvoorbeeld aan. (5 van 24)

Bulkuploads: Het uploaden van grote maphiërarchieën via Maken > Map uploaden in AEM-webinterface of het kopiëren en selecteren van &quot;Elementen plakken&quot; in Finder/Explorer in het contextmenu van de bureaubladtoepassing activeert het gebruik van dit dialoogvenster:

* Hiermee worden uploads tijdens de uitvoering weergegeven, inclusief een voortgangsbalk en de naam van het bestand dat momenteel wordt overgedragen
* Tijdens het uploaden wordt een pictogram weergegeven waarmee het uploaden wordt geannuleerd wanneer erop wordt geklikt. De overdracht wordt gestopt nadat het huidige overdrachtsbestand is voltooid
* Mislukte overdrachtsprocessen worden weergegeven met een foutbericht (alleen als de volledige overdracht mislukt)
* Als een afzonderlijk bestand niet kan worden overgedragen, wordt dit als een fout op het tabblad weergegeven. Anders worden afzonderlijke bestanden niet weergegeven op het tabblad *, maar slechts één item voor de volledige upload.

**Pictogrammen om de status van achtergrondbewerkingen** aan te geven Het toepassingspictogram geeft de status van achtergrondbewerkingen aan, zodat gebruikers een betere visuele indicatie krijgen. Als de toepassing bijvoorbeeld niet met AEM is verbonden, wordt het pictogram grijs weergegeven als er een actieve upload is, wordt er een &quot;sync&quot;-overlay weergegeven, enzovoort.

**Het vooraf ophalen van gekoppelde elementen**Om de gebruikerservaring te verbeteren bij het werken met InDesign-documenten die gekoppelde elementen bevatten die in AEM zijn opgeslagen, probeert de bureaubladtoepassing deze gekoppelde bestanden vooraf op te halen naar de lokale cache voordat deze worden gedownload en het InDesign-document wordt geopend. Op die manier heeft de gebruiker de gekoppelde bestanden lokaal beschikbaar en hoeft hij niet langer te wachten wanneer hij of zij deze in InDesign (in het deelvenster Koppelingen) opent.
Het vooraf ophalen werkt alleen als AEM de koppelingen aan de serverzijde herkent. Voor een element met herkende koppelingen wordt een lijst met verwijzingen weergegeven in de weergave Eigenschappen van het InDesign-element.

### Verbeteringen beschikbaar sinds AEM-bureaubladtoepassing 1.8.x{#enhancements-available-since-aem-desktop-app-18x}

De release van AEM-desktop app 1.8.1 met een snelle follow-up biedt verbeteringen wanneer u meerdere bestanden tegelijk opent van de AEM-gebruikersinterface naar de versie 1.8 (CQ-4237747, CQ-4238780). De verbeteringen in AEM-bureaubladtoepassing 1.8 zijn:

* Caching: nieuwe interface voor het beheer van de AEM-bureaubladtoepassingscache (CQ-4208690), inclusief
   * huidige cachegrootte weergeven
   * maximale cachegrootte definiëren voordat een melding wordt verzonden
   * De cachegrootte wordt alleen gecontroleerd bij het starten van de bureaubladtoepassing en er wordt een melding weergegeven als de geconfigureerde limiet is bereikt
   * wissen van de cacheknop is nu beschikbaar in de nieuwe interface
* Aanmelden: (Win) Vaste aanmelding bij AEM-instantie geconfigureerd voor gebruik van SAML en SSL (CQ-4216353)
* Netwerk:
   * wanneer een AEM-sessie verloopt, wordt de gebruiker nu op de hoogte gesteld en kan hij op het bericht klikken om zich opnieuw aan te melden (CQ-4202028)
   * (Mac) Voeg ondersteuning toe voor het maken van verbinding met AEM via de .pac-proxyconfiguratie (CQ-4233430)
   * (Win) los problemen op met het dialoogvenster Geavanceerd - Aanmeldings-URL (CQ-4236061)
* Bugfixes:
   * Dialoogvenster Meer informatie over element: soms was de actiebalk niet zichtbaar (CQ-4208540)
   * (Win) Het bestand kan nu worden gesynchroniseerd nadat een eerdere versie is hersteld via de gebruikersinterface van AEM Assets (CQ-4216411)

### Verbeteringen beschikbaar sinds AEM-bureaubladtoepassing 1.7{#Enhancements-Available-Since-AEM-Desktop-App-17}

* Stabiliteit:
   * Verbeterde stabiliteit wanneer de AEM-bureaubladtoepassing verbinding maakt met een overbelaste AEM-server (CQ-4224803)
   * Verbeterde stabiliteit bij het aanvragen van een groot aantal bestanden (CQ-4224212)
   * Verbeterde assetupdate met extra controle (CQ-4228291)
* Caching:
   * Schijffouten corrigeren en problemen openen bij het openen van bestanden in Photoshop, InDesign, Finder (CQ-4223993, CQ-4217603, CQ-4223717)
   * Verbeterde plaatsing in cache om binaire bestanden met een grootte van nul te voorkomen (CQ-4216599)
* Aanmelden: Verbinding maken met strictSSL uitgeschakeld voor speciale configuraties (zoals lokaal uitgegeven certificaten) (CQ-4223949)
* Netwerken: Verbeterde ondersteuning voor verbinding via netwerkproxy (CQ-4223477, CQ-4221280, CQ-4206854)
* Installatie en verwijdering:
   * (Win) Cleaner uninstallation (CQ-4220906)
   * [Windows 32bit] Installer probeert niet om het Kader van Microsoft .NET v. 4.5 (CQ-4218084) te installeren
   * (Mac) Handmatig script voor het volledig verwijderen van bureaubladtoepassingsbestanden (CQ-4216489)

>[!NOTE]
>
>Problemen die zijn aangetroffen in bètabelasting van AEM-bureaubladtoepassing 1.7 (die niet aanwezig waren in de release 1.6, worden niet vermeld in de opmerkingen bij de release).

### Verbeteringen beschikbaar sinds AEM-bureaubladtoepassing 1.6{#Enhancements-Available-Since-AEM-Desktop-App-16}

* Documentatie: Nieuwe [aanbevolen procedures voor documentatie bij de v1.x-app](https://helpx.adobe.com/experience-manager/6-3/assets/using/aem-desktop-app-best-practices.html) .
* Verbeterd aanmeldingsproces voor AEM:
   * Verbeter de behandeling van SAML * ontkoppel regels (CQ-4202781).
   * Voeg mogelijkheden toe om afzonderlijke login URL in Voorkeur (CQ-4214052, CQ-4214051) te vormen.
* Bruikbaarheid: De gebruiker op de hoogte stellen wanneer het element nog steeds wordt gedownload voor grotere elementen (CQ-4216284).
* Netwerken:
   * DNS-caching (CQ-4210176).
   * Verbinding via proxy ondersteunen in Windows (CQ-4206854).
* In cache plaatsen en toegang tot netwerkshare in Finder/Explorer:
   * Het vergrendelingspictogram is nu zichtbaar voor uitgecheckte middelen in Windows 10 (CQ-90957).
   * De inhoud van de omslag zou in netwerkaandeel kunnen verdwijnen/opnieuw verschijnen (CQ-4209160, CQ-4210180).
   * Fout bij het uploaden van een bestand als gevolg van een conflict dat is gemeld in de status van de wachtrij uploaden (CQ-4215727).
   * Bij het openen van meerdere bestanden vanuit de bureaubladtoepassingsmap in PS, worden mogelijk afgebroken of onvolledige berichten weergegeven (CQ-4216276).
* Oplossingen voor stabiliteit en prestaties:
   * Verbeterde prestaties tijdens het bladeren door mappen met veel bestanden (CQ-4214933).
   * bureaubladtoepassing 1.5 kan de bureaubladcomputer in de loop der tijd vertragen (CQ-4209159).
   * De statusfunctie voor wachtrij tonen werkt alleen voor de gebruiker die de app heeft geïnstalleerd (CQ-4212199).
   * (Windows) Zorg ervoor dat het 32-bits installatieprogramma geen 64-bits code bevat (CQ-4217406).
* Bepaalde problemen gevonden en opgelost in 1.6 bèta:
   * Hoog CPU-gebruik (CQ-4218070).
   * Sleep bestanden die een fout veroorzaken bij het uploaden naar AEM (CQ-4217006).

### Verbeteringen beschikbaar sinds AEM-bureaubladtoepassing 1.5{#Enhancements-Available-Since-AEM-Desktop-App-15}

**Versie 1.5.1.5 voor Mac OS X:** De release 1.5.1.5 biedt de volgende voordelen:

* Nieuwe en verbeterde functies: Functionaliteit Kopiëren/plakken toevoegen aan de integratie met Finder voor rechtstreekse overdracht van desktop naar AEM (CQ-4208158)
* Bugfixes:
   * Correctie van fout 43 die soms optrad tijdens het wijzigen van de naam van elementen (CQ-4207900)
   * Als u terugkeert naar een oudere versie van de tijdlijn in AEM, wordt het element niet bijgewerkt in Finder (CQ-4205194)
   * bureaubladtoepassing crasht bij bladeren door grote, geneste mappen (CQ-4208539)
   * Het koppelingspunt voor bureaubladtoepassing is nu /Volumes/DAM en is dus consistent voor alle gebruikers (CQ-4208159)
   * Wanneer u een bestand voor het eerst in InDesign plaatst, wordt een updatewaarschuwing weergegeven (CQ-4207454)

Opmerking over koppelingswaarschuwingen: In Creative Cloud-toepassingen (zoals InDesign) wordt een momentopname gemaakt van de tijd die het item het laatst heeft gewijzigd op het moment dat het wordt geplaatst. Als die datum later verandert, rapporteert de Adobe Creative Cloud-toepassing dat de koppelingen verouderd zijn. Dit wordt op een paar manieren gemeld:

* Wanneer de Adobe Creative Cloud-toepassing wordt gestart, wordt een dialoogvenster weergegeven waarin de gebruiker wordt geïnformeerd dat de gekoppelde middelen verouderd zijn en waarin de gebruiker wordt gevraagd actie te ondernemen.
* Als de Adobe Creative Cloud-toepassing al wordt uitgevoerd, wordt een geel driehoekwaarschuwingspictogram weergegeven op het gekoppelde element.

Dit gedrag is hetzelfde voor elementen op de lokale schijf en elementen in een op AEM Desktop gemonteerde map, met de volgende uitzonderingen:

* Als een geplaatst element wordt gewijzigd door een andere gebruiker, verschijnt het waarschuwingspictogram de eerste keer dat andere gebruikers een document openen dat het geplaatste element bevat. Dit gebeurt alleen als het geplaatste element al in de lokale cache is geplaatst.
* Als een gebruiker een geplaatst element wijzigt via de gekoppelde map van het AEM-bureaublad en vervolgens de lokale cache wist, wordt het geplaatste element gerapporteerd als verouderd.

Beide gevallen worden verwacht en zijn bijwerkingen van de &quot;vertraagde synchronisatie&quot;-architectuur van AEM Desktop.

**Versie 1.5.0.x voor Mac OS X en Windows:** Deze release van de AEM-bureaubladtoepassing biedt de volgende voordelen:

* Betere stabiliteit en veerkracht tegen netwerkkwesties
   * stabielere toewijzing van AEM Assets-mappen (CQ-103276, CQ-4204669, CQ-4203957)
   * Betere verwerking van bestanden in cache (CQ-4204336, CQ-4206263)
   * Verbeterde verwerking van het downloaden/uploaden van grote bestanden van meer dan 2 GB (CQ-4206438)
   * Correctie van &quot;Fout 36&quot; bij het verplaatsen of hernoemen van een groter aantal bestanden in Finder (CQ-4204640)
* Optimalisaties in netwerkcommunicatie met AEM Server (CQ-4204974, CQ-100903)
* Betere betrouwbaarheid bij het openen, plaatsen en opslaan van AEM-middelen in Creative Cloud-apps (CQ-4203968, CQ-4205511, CQ-103543, CQ-4207141, CQ-90980)
* Verbeterde ondersteuning: optie voor het wissen van de cache (CQ-4202541), eenvoudige toegang tot logbestanden (CQ-4202340, CQ-4204673)
* Andere correcties:
   * Betere ondersteuning voor elementen en mappen met Japanse tekens in naam/niet-Engelse taalinstellingen (CQ-4195433, CQ-4205793, CQ-4199446)
   * Betere afhandeling van aanmelding met SSL (CQ-4200217)
   * Betere aandelenmontage (CQ-42007-93)
   * Verschillende verbeteringen in de stabiliteit (CQ-4207539, CQ-4200378)
   * Betere verwerking van URL voor AEM-middelen in Voorkeuren (CQ-97388)

### Verbeteringen beschikbaar sinds AEM-bureaubladtoepassing 1.4{#Enhancements-Available-Since-AEM-Desktop-App-14}

* Het eenvoudig uploaden van hiërarchische mappen via de nieuwe handeling Maken > Map uploaden in Touch UI
   * Handeling start een bewerking voor het uploaden van mappen die wordt uitgevoerd door de bureaubladtoepassing
   * Bureaubladtoepassing doorloopt de opgegeven maphiërarchie op het bureaublad op de achtergrond en uploadt de bestanden naar AEM-middelen
   * De gebruiker kan de vooruitgang in het nieuwe Upload venster van de Status van de Rij met vooruitgangsbar voor aan de gang zijnde verrichtingen controleren
   * De status van de wachtrij uploaden biedt ook betere informatie over probleemoplossing (bijvoorbeeld geen verbinding met de server)
* Nieuwe handeling Bewerken in Touch-gebruikersinterface waarin bewerkingen voor uitchecken en openen in één handeling worden gecombineerd
* Geoptimaliseerde groepering van acties die betrekking hebben op het bureaublad in Touch UI (AEM 6.3)
* Verbeterde compatibiliteit met de nieuwste versies van het besturingssysteem
* Door de klant gemelde correcties

### Verbeteringen beschikbaar sinds AEM-bureaubladtoepassing 1.3{#Enhancements-Available-Since-AEM-Desktop-App-13}

* Meer efficiëntie. De gebruikers besteden minder tijd wachtend op netwerkverrichtingen om te voltooien.
* Verbeterde integratie met de Finder, die meer stabiliteit en toegang tot functies, zoals miniaturen, biedt.
* Verbeteringen in cache en prestaties.
* Betere ondersteuning voor het rechtstreeks opslaan van desktopapps (PS, ID, AI, enzovoort).
* Verbeterde integratie met Mac OS (het protocol voor lokale netwerkstations is veranderd van WebDAV in stabielere SMB1).
* Desktop-app maakt verbinding met de AEM-server via het native HTTP RESTful-protocol van AEM.
* Bestanden worden eerst lokaal opgeslagen en vervolgens na een vooraf gedefinieerde tijd (30 seconden) weer naar AEM geüpload. Hierdoor wordt de tijd voor het opslaan van bestanden verkort.
* Betere verwerking van bureaubladtoepassingen die tussentijdse bestandsbewerkingen gebruiken om een bestand op te slaan (gedeeltelijke opslag en tijdelijke bestanden), waardoor de tijdlijn van AEM Asset de juiste versie en informatie over het uploaden van middelen kan weergeven.
* Dialoogvenster voor het bijhouden van de status van uploadtaken op de achtergrond.

## Lijst met wijzigingen {#list-of-changes}

### Koppelpunt op Mac {#mount-point-on-mac}

Sinds Mac OS 10.12 (Sierra) heeft Apple de machtigingen voor de map /Volumes die wordt gebruikt voor het koppelen van netwerkstations en apparaten gewijzigd in meer beperkingen. Voor het maken van een nieuw koppelingspunt zijn administratieve rechten vereist. Dit probleem is opgelost in Mac OS 10.12.5.

Aangezien de AEM-bureaubladtoepassing moet worden uitgevoerd voor gebruikers die geen beheerrechten hebben op de lokale computer, is het koppelingspunt voor de AEM-middelenopslagplaats in 1.4 en 1.5 gewijzigd in een DAM-submap in de lokale map van de gebruiker op MacOS (CQ-104183).

Aangezien de map /Volumes geen beheerrechten meer vereist, is deze wijziging in 1.5.1 ongedaan gemaakt. Hierdoor kunt u ook InDesign-documenten delen die AEM-elementen tussen MacOS-gebruikers hebben geplaatst.

### Protocol wijzigen (sinds v1.3) {#protocol-change-since}

* Mac OS X:
   * Het lokale protocol van de netwerkaandrijving voor OS X Desktopintegratie veranderde in SMB1 van WebDAV.
   * De AEM-opslagplaats die is gekoppeld met de bureaubladtoepassing is zichtbaar als een &#39;smb&#39;-netwerkstation in Finder in plaats van als een WebDAV-station.
* Windows:
   * Het lokale protocol van de netwerkaandrijving voor de Desktopintegraties van Vensters blijft; AEM wordt gemonteerd als een WebDAV-share.
* Voor beide platforms (Windows en Mac):
   * Het protocol voor toegang tot/download van middelen en voor het uploaden van wijzigingen naar AEM is gewijzigd in het native AEM-protocol, dat een op HTTP gebaseerd RESTful-protocol is. Het verstrekt grotere controle over netwerkverrichtingen en is meer compatibel met de netwerkinfrastructuur.

>[!NOTE]
>
>In Mac OS X leidt de wijziging van het lokale netwerkschijfprotocol van WebDAV in SMB1 tot een ander lokaal pad naar hetzelfde middel in de opslagplaats. Dit kan gevolgen hebben voor koppelingen naar bestanden die in Adobe Creative Cloud-toepassingen worden geplaatst via de opdracht Plaatsen. Raadpleeg de app [AEM Desktop](use-app-v1.md) gebruiken voor meer informatie.

### Bestandsbeheer (sinds 1.3) {#file-handling-since}

* Mappen worden automatisch bijgewerkt na een vooraf gedefinieerde vertraging (momenteel 30 seconden).
* Bestanden die door andere gebruikers zijn uitgecheckt, zijn gemarkeerd als alleen-lezen.
* Bestanden worden in twee fasen opgeslagen op een netwerkstationlocatie die via de bureaubladtoepassing is geïnstalleerd.
* In de eerste fase wordt een bestand lokaal opgeslagen. Op deze manier hoeft de gebruiker die het bestand opslaat, niet te wachten totdat het bestand volledig naar AEM is overgebracht en kan het werk worden hervat zodra het bestand is opgeslagen.
* In de tweede fase uploadt de bureaubladtoepassing een bijgewerkt bestand naar de AEM-server na een vooraf gedefinieerde vertraging (bijvoorbeeld dertig jaar). Deze bewerking vindt plaats op de achtergrond. Met de optie Status **achtergrondbestandssync** tonen kunt u de status van de uploadbewerking weergeven.

## Belangrijke kennisgevingen {#important-notices}

**Map uploaden.** Het wordt aanbevolen om de nieuwe mogelijkheid voor het uploaden van mappen te gebruiken om grotere, hiërarchische mappen te uploaden naar AEM in plaats van een kopie/sleep en zet deze neer in een gekoppelde AEM-opslagplaats vanuit Finder-/Verkenner-niveau. Als u de functie voor het uploaden van mappen gebruikt, communiceert de bureaubladtoepassing rechtstreeks met AEM en heeft deze dus veel meer controle over het gehele proces.

**AEM-sessie beschikbaar houden.** De AEM-bureaubladtoepassing is afhankelijk van een sessie die voor de AEM Assets-server is geopend om de juiste werking te garanderen. Voor gebruikers die elke dag met Desktop app werken, wordt geadviseerd om AEM Middelen aan het eind van hun dag te ontkoppelen om logout af te dwingen, en dan &quot;te monteren AEM Middelen&quot;in de ochtend om ervoor te zorgen zij worden het programma geopend en het netwerkaandeel operationeel is.

**Schakel Pictogramvoorvertoning uit in Finder.** Als u met Finder wilt bladeren door grote mappen, met name door slechte netwerkconnectiviteit, moet u ervoor zorgen dat zowel &quot;Pictogram&quot; als &quot;Voorvertoning pictogram&quot; is uitgeschakeld. Anders, zal de Vinder beginnen elk middel in een omslag te downloaden om een kleine voorproef te produceren, die tot slechte prestaties en hoog bandbreedtegebruik (CQ-4219779) kan leiden

* Ga naar de gedeelde netwerkmap met AEM Assets
* Klik met de rechtermuisknop op het DAM-koppelingspunt
* Weergaveopties tonen selecteren
* Selectie van Voorvertoning pictogram tonen opheffen
* Klik op &quot;Als standaardwaarden gebruiken&quot;

**Cache opschonen wanneer verbinding wordt gemaakt met een nieuwe AEM-server.** Als de bureaubladtoepassing verbinding maakt met een andere AEM-server met dezelfde URL, wordt de cache niet automatisch gewist. Cache handmatig wissen om de juiste bewerkingen te garanderen. Dit gebeurt normaal gesproken tijdens het testen, wanneer AEM-installaties kunnen worden vervangen terwijl ze op dezelfde URL worden uitgevoerd (CQ-4216982)

**Gebruik CA-ondertekende SSL-certificaten.** Houd er rekening mee dat de AEM-bureaubladtoepassing zelfondertekende SSL-certificaten niet ondersteunt wanneer verbinding wordt gemaakt met AEM via een beveiligde HTTPS-verbinding. Voor dergelijke verbindingen is op de server een certificaat met CA-handtekening vereist. (CQ-87941)

## Known issues {#known-issues}

* Algemeen:
   * Server-URL&#39;s moeten naar de server verwijzen zonder een pad (bijvoorbeeld `http://server`, `https://server`, `http://server:port`, of `https://server:port`). Contextpaden en andere submappen dan /content/dam worden niet ondersteund (CQ-89343, CQ-87272)
* Bestandsnamen/lokalisatie:
   * Bestands- en mapnamen met gereserveerde tekens worden niet correct verwerkt. Gebruik bestands- en mapnamen die voldoen aan de AEM-vereisten (CQ-93361, CQ-93308, CQ-89276, CQ-4217183)
   * Sommige toepassingen, zoals Adobe Illustrator, maken mogelijk bestanden met namen die niet worden ondersteund in AEM. Bijvoorbeeld, toevoegend `Converted` na het omzetten van een dossier, dat het verhindert worden geupload (CQ-4216985)
   * Middelen met internationale namen kunnen verschijnen en elke paar seconden verdwijnen
* Inchecken en uitchecken:
   * Een element dat door een gebruiker is uitgecheckt, kan niet door een andere gebruiker worden geopend, door de handeling Openen vanuit de aanraakinterface of rechtstreeks op het bureaublad. Sommige toepassingen melden het als gesloten, maar ook bedorven of zelfs hangen terwijl het proberen te openen. (CQ-4199234)
   * Het gelijktijdig wijzigen van bestanden door meerdere gebruikers kan tot gevolg hebben dat sommige wijzigingen verloren gaan. De oplossing hiervoor is de incheck- en uitcheckfunctie te gebruiken om te voorkomen dat meerdere gebruikers hetzelfde bestand wijzigen (CQ-97035)
   * Bepaalde toepassingen ondersteunen de alleen-lezen markering niet op de juiste wijze, waardoor een gebruiker een bestand kan opslaan dat door een andere gebruiker is uitgecheckt. Het gewijzigde bestand wordt pas overgedragen wanneer de andere gebruiker het bestand incheckt. Beide wijzigingen zijn beschikbaar in AEM als verschillende versies van het element (CQ-89551, CQ-87572, CQ-89615)
   * De status voor Uitchecken en Alleen-lezen wordt onafhankelijk gerapporteerd in Finder. Dit resulteert in 2 vergrendelingspictogrammen wanneer een gebruiker een middel uitcheckt (CQ-89507)
* Integratie van Finder:
   * Wanneer u grote bestanden sleept of neerzet, kan de Finder de tijd uit nemen terwijl bestanden op de achtergrond worden overgebracht. Dit leidt tot een `Error - 36`. U kunt dit probleem omzeilen door het element opnieuw te slepen/neer te zetten of te openen (CQ-4219628)
   * Het handmatig opnieuw laden van mappen werkt niet altijd. Oplossing:  Wacht 30 seconden voordat de map automatisch wordt bijgewerkt. (CQ-97389)
   * Meer informatie over middelen... is beperkt tot één bestandsselectie (CQ-89542, CQ-87656)
   * Openen in AEM-elementen... is beperkt tot één bestand en één map (CQ-83382)
   * Fout bij het wijzigen van de naam van elementen zonder extensie (CQ-4218971)
* Functionaliteit voor kopiëren en plakken: Plakken is beschikbaar wanneer er geen element naar het klembord is gekopieerd
* Windows:
   * Bestanden met alternatieve gegevensstromen (ADS) worden alleen volledig ondersteund op NTFS. Als dergelijke bestanden worden gekopieerd naar het WebDAV-aandeel dat door de bureaubladtoepassing wordt geleverd, wordt de gebruiker gewaarschuwd dat het bestand eigenschappen heeft die niet naar de nieuwe locatie kunnen worden gekopieerd. Dit is meestal prima omdat de eigenschappen alleen relevant zijn voor een bepaalde toepassing op het bureaublad van de gebruiker en niets te maken hebben met de feitelijke bestandsinhoud (CQ-103770) (Win)
   * desktop app in Windows moet worden geïnstalleerd door de gebruiker die de app gaat gebruiken (CQ-4216389) (win)
   * De app kan vastlopen wanneer op de knop Opnieuw proberen op een mislukte upload wordt geklikt onder bepaalde omstandigheden nadat de batchupload is hervat nadat de verbinding is verbroken (CQ-4251884) (Win)

## Nuttige bronnen {#helpful-resources}

* [AEM-documentatie](https://helpx.adobe.com/nl/support/experience-manager/6-4.html)
* [AEM-bureaubladtoepassing v1.x gebruiken](use-app-v1.md)
* [Aanbevolen werkwijzen voor AEM-bureaubladtoepassing v1.x](best-practices-for-v1.md)

## Compatibiliteitsmatrix en voorwaarden {#compatibilitymatrix}

De AEM-bureaubladtoepassing werkt met verschillende versies van AEM. Zie de compatibiliteitsmatrix voor de ondersteunde versies.

| Versie | Herziening | Releasedatum | Compatibiliteit |
|---------|------------------------|--------------|-------------------------------------------------------------|
| 1.10 | 1.10.0.3 (Mac en Windows) | 31 aug. 2018 | AEM 6.5; AEM 6.4 SP1; AEM 6.3 SP2; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
| 1.9 | 1.9.1.1 (Mac en Windows) | 21 jun. 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
| 1.8 | 1.8.1.0 (Mac en Windows) | 28 mrt. 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
| 1.7 | 1.7.0.3 (Mac en Windows) | 10 jan. 2018 | AEM 6.3 SP1; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
