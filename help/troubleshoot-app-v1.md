---
title: AEM-bureaubladtoepassing versie 1.x problemen oplossen
description: Los AEM Desktop app versie 1.x problemen op om de af en toe kwesties met betrekking tot installatie, verbetering, configuratie, etc. op te lossen.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a18aa9c3dad8802c3de929ba4ebb1a1583b47165

---


# Problemen met AEM-bureaubladtoepassing v1.x oplossen {#troubleshoot-aem-desktop-app}

Los AEM- Desktopapp problemen op om de af en toe kwesties met betrekking tot installatie, verbetering, configuratie, etc. op te lossen.

De Adobe Experience Manager (AEM)-bureaubladtoepassing bevat hulpprogramma&#39;s waarmee u de AEM Assets-opslagplaats kunt toewijzen als een gedeelde netwerkverbinding op het bureaublad (SMB-share op Mac OS). Het aandeel van het netwerk is een werkend systeemtechnologie die verre bronnen toelaat worden behandeld alsof zij deel van het lokale dossiersysteem van een computer maakten. In het geval van een bureaubladtoepassing wordt de DAM-opslagstructuur (Digital Asset Management) van een externe AEM-instantie aangewezen als externe bestandsbron. In het volgende diagram wordt de topologie van de bureaubladtoepassing beschreven:

![bureaubladtoepassingsdiagram](assets/aem-desktopapp-architecture.png)

Met deze architectuur, onderschept de Desktop toepassing dossiersysteemvraag (open, dicht, lees, schrijf, etc.) aan het opgezette netwerkaandeel, en zet hen in inheemse vraag van HTTP AEM aan de server van AEM om. Bestanden worden lokaal in cache geplaatst. Zie AEM-bureaubladtoepassing v1.x [gebruiken voor meer informatie](use-app-v1.md).

## Overzicht van de AEM-bureaubladtoepassing {#desktop-app-component-overview}

desktop-app bevat de volgende componenten:

* **De bureaubladtoepassing**: De toepassing monteert of ontkoppelt DAM als ver dossiersysteem, en vertaalt dossiersysteemvraag tussen het plaatselijk opgezette netwerkaandeel en de verre instantie AEM waarmet het verbindt.
* **Besturingssysteem WebDAV/SMB-client**: Verwerkt de communicatie tussen Windows Verkenner/Finder en de desktop-app. Als een bestand wordt opgehaald, gemaakt, gewijzigd, verwijderd, verplaatst of gekopieerd, communiceert de WebDAV/SMB-client van het besturingssysteem deze bewerking naar de desktop-app. Nadat de communicatie is ontvangen, zet de bureaubladtoepassing deze om in externe API-aanroepen van AEM. Als een gebruiker bijvoorbeeld een bestand maakt in de gekoppelde map, initieert de WebDAV/SMB-client een aanvraag, die de desktop-app omzet in een HTTP-aanvraag die het bestand maakt in DAM. De WebDAV/SMB-client is een ingebouwde component van het besturingssysteem. Het is op geen enkele manier verbonden met een bureaubladtoepassing, AEM of Adobe.
* **Adobe Experience Manager-exemplaar**: Biedt toegang tot elementen die zijn opgeslagen in de DAM-opslagplaats van AEM Assets. Bovendien voert het acties uit die door Desktop app namens de lokale Desktoptoepassingen worden gevraagd interactie met het opgezette netwerkaandeel. De AEM-doelinstantie moet AEM versie 6.1 of hoger uitvoeren. Voor AEM-instanties met eerdere AEM-versies zijn mogelijk extra functiepakketten en hotfixes vereist die zijn geïnstalleerd om volledig te kunnen functioneren.

## Beoogde gebruiksgevallen voor AEM-bureaubladtoepassing {#intended-use-cases-for-aem-desktop-app}

De AEM-bureaubladtoepassing gebruikt de technologie voor netwerkdeling om een externe AEM-opslagplaats toe te wijzen aan een lokale desktop. Het is echter niet bedoeld als vervanging voor een netwerkshare-holding-assets, waarbij gebruikers digitale middelenbeheerbewerkingen rechtstreeks vanaf hun lokale bureaublad uitvoeren. Dit zijn onder andere het verplaatsen of kopiëren van meerdere bestanden of het rechtstreeks slepen van grote mapstructuren naar het gedeelde netwerk van AEM Assets in Finder/Explorer.

De AEM-bureaubladtoepassing biedt een handige manier om DAM-middelen te openen en bewerken (opslaan) tussen de AEM Assets Touch-interface en het lokale bureaublad. Elementen op de AEM Assets-server worden gekoppeld aan uw workflows op het bureaublad.

Het volgende voorbeeld illustreert hoe AEM Desktop zou moeten worden gebruikt:

* Een gebruiker meldt zich aan bij AEM en gebruikt Web UI om van activa de plaats te bepalen.
* Met de actiemogelijkheden van het bureaublad van de AEM-webinterface opent, geeft of bewerkt de gebruiker het middel desgewenst op het bureaublad.
* AEM Desktop opent de activa in de standaardredacteur voor het dossiertype van activa.
* De gebruiker brengt de gewenste wijzigingen aan in het element.
* Nadat een bestand is gewijzigd, kan de gebruiker de synchronisatiestatus van het bestand weergeven via het statusvenster voor achtergrondsynchronisatie van AEM Desktop.
* Met het contextmenu van AEM Desktop, controleert de gebruiker in/uit het middel, of keert aan het DAM gebruikersinterface terug.
* Nadat de wijzigingen in het bestand zijn voltooid, keert de gebruiker terug naar de AEM-webinterface

Dit is niet het enige gebruiksgeval. Het toont echter aan hoe AEM Desktop een handig mechanisme is om elementen lokaal te openen/bewerken. U wordt aangemoedigd om de DAM-webinterface zoveel mogelijk te gebruiken, omdat deze een betere ervaring biedt. Het biedt Adobe meer flexibiliteit om aan de vereisten van de klant te voldoen.

## Beperkingen {#limitations}

WebDAV/SMB1 netwerkaandeel verstrekt het gemak om met dossiers in een venster van de Ontdekkingsreiziger/van de Vinder te werken. Nochtans, communiceren de Ontdekkingsreiziger/de Vinder en AEM over een netwerkverbinding die bepaalde beperkingen heeft. De tijd die bijvoorbeeld nodig is om een 1-GB-bestand naar de gekoppelde WebDAV/SMB-map te kopiëren, is ongeveer gelijk aan de tijd die nodig is om een 1-GB-bestand met een webbrowser naar een website te uploaden. In het eerste geval kan de duur langer zijn vanwege inefficiënties van het WebDAV/SMB-protocol en de WebDAV/SMB-clients van het besturingssysteem (in het bijzonder Mac OS X).

Er zijn beperkingen aan de typen taken die vanuit een gekoppelde map kunnen worden uitgevoerd. Over het algemeen kan het lastig zijn om met grote bestanden te werken, met name via een slechte/hoge latentie/lage bandbreedte-netwerkverbinding, vooral wanneer u grote bestanden bewerkt.

Adobe raadt u aan een aantal tests met hoofdletters en kleine letters uit te voeren voordat u een client bindt, zodat bepaalde bestandstypen op een efficiënte manier op hun plaats kunnen worden bewerkt vanuit de gekoppelde map.

AEM Desktop is niet geschikt voor intensieve manipulatie van bestandssystemen, waaronder, maar niet beperkt tot:

* Bestanden en mappen verplaatsen of kopiëren
* Veel elementen toevoegen aan AEM
* Bestanden zoeken en openen via het bestandssysteem, behalve in mappen
* Bestandsarchieven comprimeren of decomprimeren

Vanwege beperkingen in het besturingssysteem geldt voor Windows een maximale bestandsgrootte van 4.294.967.295 bytes (ongeveer 4,29 GB). Dit is te wijten aan een registerinstelling die bepaalt hoe groot een bestand op een netwerkshare kan zijn. De waarde van de registratie het plaatsen is DWORD met een maximumgrootte die het referenced aantal evenaart.

De desktop-app van Experience Manager beschikt niet over een configureerbare time-outwaarde die de verbinding tussen de Experience Manager-server en de desktop-app verbreekt na een vast tijdsinterval. Wanneer u grote middelen uploadt en de verbinding na een tijdje wordt verbroken, probeert de toepassing het element een paar keer te uploaden door de time-out van het uploaden te verhogen. Er is geen aanbevolen manier om de standaardtime-outinstellingen te wijzigen.

## Caching en communicatie met AEM {#caching-and-communication-with-aem}

De AEM-bureaubladtoepassing biedt interne mogelijkheden voor caching en het uploaden naar de achtergrond om de gebruikerservaring te verbeteren. Wanneer u een groot bestand opslaat, wordt het eerst lokaal opgeslagen zodat u kunt doorgaan met werken. Na enige tijd (momenteel 30 seconden) wordt het bestand op de achtergrond naar de AEM-server verzonden.

In tegenstelling tot Creative Cloud Desktop of andere oplossingen voor bestandssynchronisatie, zoals Microsoft One Drive, is de AEM-bureaubladtoepassing geen volledige Desktop Sync client. De reden hiervoor is dat het toegang biedt tot de gehele AEM Assets-opslagplaats, die zeer groot kan zijn (honderden gigabytes of terabytes) voor een volledige synchronisatie.

Caching verstrekt de capaciteit om de netwerk/opslagoverheadkosten tot slechts een ondergroep van activa te beperken die voor de gebruiker relevant zijn.

>[!CAUTION]
>
>Adobe raadt u aan miniatuurgeneratie uit te schakelen om sneller te kunnen bladeren. Als u pictogramvoorvertoningen inschakelt, plaatst de app de digitale elementen in de cache wanneer u door de gekoppelde map navigeert. De app downloadt ook elementen die de gebruiker niet kan schelen, waardoor het laden aan de server wordt toegevoegd, de bandbreedte van de gebruiker wordt verbruikt en meer schijfruimte van de gebruiker wordt gebruikt.

Zo voert de AEM-bureaubladtoepassing caching uit:

* Wanneer u een map opent in Finder en er miniaturen/voorvertoningen van bestanden worden weergegeven, of wanneer u een bestand opent in een toepassing, plaatst de bureaubladtoepassing het bestand binair in de cache.
* Wanneer u bestanden opslaat via Finder of andere bureaubladtoepassingen, wordt het bestand eerst lokaal opgeslagen (in cache geplaatst) en wordt het besturingssysteem op de hoogte gesteld. Het bestand wordt vervolgens in de wachtrij geplaatst voor uploaden naar de server op de achtergrond en wordt uiteindelijk via het netwerk geüpload. In het geval van een netwerkfout probeert de bureaubladtoepassing het gehele bestand maximaal drie keer te uploaden. Als het uploaden van de bestanden mislukt nadat drie keer is geprobeerd, wordt het bestand gemarkeerd als een conflicterend bestand en wordt de status weergegeven via het venster Status wachtrij uploaden op de achtergrond. bureaubladtoepassing probeert het bestand niet meer bij te werken. De gebruiker moet het bestand bijwerken en opnieuw uploaden nadat de connectiviteit is hersteld

Elke bewerking wordt niet lokaal in het cachegeheugen opgeslagen. Het volgende wordt onmiddellijk zonder lokale caching naar de AEM-server verzonden:

* Alle bewerkingen in mappen, zoals maken, verwijderen, enzovoort
* Met de functie Map uploaden die in versie 1.4 is geïntroduceerd, wordt een lokale maphiërarchie geüpload zonder de bestanden lokaal in de cache te plaatsen

## Individuele verrichtingen {#individual-operations}

Wanneer het oplossen van problemen sub-geoptimaliseerde prestaties voor individuele gebruikers, eerste herzie [Beperkingen](https://helpx.adobe.com/experience-manager/desktop-app/troubleshooting-desktop-app.html#limitations). De volgende secties bevatten suggesties om de prestaties voor individuele gebruikers te verbeteren.

## Aanbevelingen voor bandbreedte {#bandwidth-recommendations}

De bandbreedte beschikbaar aan een individuele gebruiker speelt een kritieke rol in de prestaties van de cliënt WebDAV/SMB.

Adobe raadt aan dat de uploadsnelheid van een individuele gebruiker dichtbij 10 Mbps ligt. Voor draadloze verbindingen, wordt de bandbreedte vaak gedeeld tussen veelvoudige gebruikers. Als de veelvoudige gebruikers tegelijkertijd taken uitvoeren die netwerkbandbreedte verbruiken, kunnen de prestaties nog verder degraderen. Gebruik een bekabelde verbinding om dergelijke problemen te voorkomen.

## Windows-specifieke configuraties {#windows-specific-configurations}

Als u AEM in Windows uitvoert, kunt u Windows configureren om de prestaties van de WebDAV-client te verbeteren. Ga voor meer informatie naar [https://support.microsoft.com/en-us/kb/2445570](https://support.microsoft.com/en-us/kb/2445570).

In Windows 7 kunt u de prestaties van WebDAV verbeteren door IE-instellingen te wijzigen. Ga voor meer informatie naar [http://oddballupdate.com/2009/12/fix-slow-webdav-performance-in-windows-7/](http://oddballupdate.com/2009/12/fix-slow-webdav-performance-in-windows-7/).

## Gelijktijdige bewerkingen {#concurrent-operations}

Wanneer u lokaal met een bestand werkt, controleert AEM Desktop of een nieuwere versie van het bestand beschikbaar is in AEM. Als er een nieuwe versie beschikbaar is, downloadt de toepassing een nieuwe kopie van het bestand naar de lokale cache. AEM Desktop overschrijft een lokaal in de cache opgeslagen bestand echter niet als het is gewijzigd. Met deze functie voorkomt u dat uw werk per ongeluk wordt overschreven.

Wanneer hetzelfde bestand zowel lokaal als in AEM wordt gewijzigd, overschrijft de lokaal gewijzigde versie de versie in AEM. In dit geval is de vorige versie beschikbaar in de tijdlijn van het element. U kunt beide versies controleren en eventuele conflicten oplossen.

Als een lokaal bestand niet overeenkomt met de versie die beschikbaar is op de server, wordt in het statusdialoogvenster voor uploaden op de achtergrond melding gemaakt van het conflict. Open het conflicterende bestand en sla het op om het probleem op te lossen. Als u het bestand opslaat, synchroniseert AEM Desktop de laatste lokale wijzigingen in AEM. U kunt vorige versies van het element in de tijdlijn bekijken en eventuele conflicten oplossen.

U moet rekening houden met extra factoren wanneer meerdere gebruikers proberen te werken in afzonderlijke gekoppelde mappen die hetzelfde AEM-exemplaar als doel hebben. De volgende factoren zijn met name van belang:

* De hoeveelheid bandbreedte beschikbaar op het van gebruikers voortkomende netwerk
* De configuratie van het netwerk, zoals firewalls of volmachten, van het voortkomende netwerk
* Hoeveelheid bandbreedte beschikbaar in het netwerk van de doel-AEM-instantie
* Of een verzender aanwezig is vóór de AEM-doelinstantie
* Huidige belasting op de AEM-doelinstantie

## Aanvullende AEM-configuraties {#additional-aem-configurations}

Als de WebDAV/SMB prestaties drastisch degraderen wanneer de veelvoudige gebruikers gelijktijdig werken, kunt u een paar dingen in AEM vormen, die kunnen helpen prestaties verbeteren.

## Workflows voor middelentransitie bijwerken {#update-asset-transient-workflows}

U kunt de prestaties aan AEM-zijde verbeteren door tijdelijke workflows in te schakelen voor de DAM Update Asset-workflow. Als u tijdelijke workflows inschakelt, wordt de vereiste verwerkingscapaciteit voor het bijwerken van middelen verminderd wanneer deze worden gemaakt of gewijzigd in AEM.

1. Navigeer naar `/miscadmin` in de instantie AEM die (bijvoorbeeld, `http://[Server]:[Port]/miscadmin`) moet worden gevormd.
1. Vouw in de navigatiestructuur **Gereedschappen** > **Workflow** > **Modellen** > **dam** uit.
1. Dubbelklik op **DAM Update Asset**.
1. Ga in het zwevende gereedschapsvenster naar het tabblad **Pagina** en klik vervolgens op **Pagina-eigenschappen**.
1. Schakel het selectievakje **Tijdelijk werkschema** in en klik op **OK**.

### De tijdelijke Granite-workflowwachtrij aanpassen {#adjust-granite-transient-workflow-queue}

Een andere methode om de prestaties van AEM te verbeteren is de waarde van de maximumparallelle banen voor de de baan van de Rij van de Rij van het Werkschema van de Overgang van de Granite te vormen. De aanbevolen waarde is ongeveer de helft van het aantal CPU&#39;s dat beschikbaar is op de server. Voer de volgende stappen uit om de waarde aan te passen:

1. Navigeer naar */system/console/configMgr* in de AEM-instantie die moet worden geconfigureerd (bijvoorbeeld <http://&lt;Server&gt;:&lt;Port&gt;/system/console/configMgr>).
1. Zoek naar **QueueConfiguration**, en klik om elke baan te openen tot u van de **Granite Transient Workflow Queue** baan de plaats bepaalt. Klik op het pictogram Bewerken ernaast.
1. Wijzig de waarde voor **Maximale parallelle taken** en klik op **Opslaan**.

## AWS-configuratie {#aws-configuration}

Vanwege de beperkingen van de netwerkbandbreedte kunnen de prestaties van WebDAV/SMB afnemen wanneer meerdere gebruikers gelijktijdig werken. Adobe raadt u aan de AWS-instantie voor een AEM-doelinstantie die op AWS wordt uitgevoerd, uit te breiden om de prestaties van WebDAV/SMB te verbeteren.

Deze maatregel verhoogt specifiek de hoeveelheid netwerkbandbreedte beschikbaar aan de server. Hier volgen enkele details:

* De hoeveelheid netwerkbandbreedte die aan een instantie AWS wordt gewijd neemt toe aangezien de grootte van de instantie stijgt. Zie de [AWS-documentatie](https://aws.amazon.com/ec2/instance-types/)voor informatie over hoeveel bandbreedte beschikbaar is voor elke instantiegrootte.
* Bij het oplossen van problemen voor een grote cliënt, vormde Adobe de grootte van zijn instantie AEM aan c4.8xlarge, hoofdzakelijk voor 4000 Mbps van specifieke bandbreedte die het verstrekt.
* Als er een verzender vóór de instantie AEM is, zorg ervoor dat het van aangewezen grootte is. Als de instantie AEM 4000 Mbps verstrekt maar de verzender slechts 500 Mbps verstrekt, is de efficiënte bandbreedte slechts 500 Mbps. Dit komt doordat de verzender een knelpunt in het netwerk maakt.

## Beperkingen van uitgecheckte bestanden {#checked-out-file-limitations}

Er zijn een paar bekende beperkingen in de manier u met uitgecheckte dossiers door Ontdekkingsreiziger/Vinder kunt in wisselwerking staan. Als een bestand is uitgecheckt, moet het alleen-lezen zijn voor iedereen behalve de gebruiker die het bestand heeft uitgecheckt. De implementatie van het WebDAV/SMB1-protocol in AEM dwingt deze regel af. Maar WebDAV/SMB-clients van het besturingssysteem communiceren vaak niet netjes met uitgecheckte bestanden. Enkele oddities worden hieronder beschreven.

### Algemeen {#general}

Bij het schrijven naar een uitgecheckt bestand wordt de vergrendeling alleen afgedwongen binnen de AEM WebDAV-implementatie. Dit betekent dat de vergrendeling alleen wordt afgedwongen door clients die WebDAV gebruiken, zoals de bureaubladtoepassing. Het slot wordt niet afgedwongen via AEM-webinterface. In de AEM-interface wordt alleen een vergrendelingspictogram weergegeven in de kaartweergave voor elementen die zijn uitgecheckt. Het pictogram is cosmetisch en heeft geen invloed op het gedrag van AEM.

Over het algemeen gedragen de WebDAV-clients zich niet altijd zoals u had verwacht. Er kunnen nog andere problemen zijn. Het vernieuwen of controleren van het element in AEM is echter een goede manier om te controleren of een element niet wordt gewijzigd. Dit gedrag is typisch voor de OS WebDAV cliënten, die niet onder de controle van Adobe zijn.

### Windows {#windows}

Het verwijderen van een bestand lijkt te zijn gelukt omdat het bestand verdwijnt uit de bestandsverkenner in Windows. Als u de map echter vernieuwt en AEM-elementen controleert, ziet u dat het bestand nog steeds aanwezig is. Bovendien lijkt het bewerken van bestanden te zijn geslaagd (er worden geen waarschuwingsvensters of foutberichten weergegeven). Als u het bestand echter opnieuw opent of AEM-elementen controleert, wordt duidelijk dat het bestand ongewijzigd blijft.

#### Mac OS X {#mac-os-x}

Bij het vervangen van een bestand wordt geen waarschuwing of fout weergegeven, maar bij het controleren van het element in AEM wordt duidelijk dat het bestand ongewijzigd blijft. Vernieuw of controleer de activa in AEM om te verifiëren dat het niet wordt gewijzigd.

## Problemen met bureaubladpictogrammen oplossen (Mac OS X) {#troubleshooting-desktop-app-icon-issues-mac-os-x}

Nadat u de bureaubladtoepassing hebt geïnstalleerd, verschijnt het pictogram van het menu voor de bureaubladtoepassing in de menubalk. Als het pictogram niet wordt weergegeven, voert u de volgende stappen uit om het probleem op te lossen:

1. Open het eindvenster van het besturingssysteem.
1. Typ het volgende bevel bij de bevelherinnering, en druk dan binnengaan:

   ```shell
    cd ../Library/Caches.
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   rm -r com.adobe.aem.assetscompanion 
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   cd ~/Library/Preferences
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   rm com.adobe.aem.assetscompanion.plist
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   rm ~/Library/Group\ Containers/group.com.adobe.aem.desktop/*
   ```

1. Start het systeem opnieuw.

AEM Desktop probeert om het even welk bepaald dossier drie keer te synchroniseren. Als het bestand na de derde poging niet kan worden gesynchroniseerd, wordt het bestand door AEM Desktop als een conflict beschouwd en wordt u via het statusvenster voor uploaden op de achtergrond op de hoogte gebracht. Een conflictstatus geeft aan dat uw laatste wijzigingen nog steeds lokaal beschikbaar zijn, maar niet worden gesynchroniseerd met AEM. AEM-bureaubladtoepassing probeert niet meer te synchroniseren.

U kunt deze situatie het eenvoudigst verhelpen door het conflicterende bestand te openen en opnieuw op te slaan. Het dwingt AEM Desktop om synchronisatie voor extra drie gelegenheden te proberen. Raadpleeg de onderstaande secties voor meer informatie als het bestand nog steeds niet kan worden gesynchroniseerd.

## AEM Desktop-cache wissen {#clearing-aem-desktop-cache}

Het wissen van het cachegeheugen van AEM Desktop is een voorlopige taak voor het oplossen van problemen die verschillende AEM Desktop-problemen kan oplossen.

U kunt de cache wissen door de cachemap van de toepassing op de volgende locaties te verwijderen: Windows: %LocalAppData%\Adobe\AssetsCompanion\Cache\

Mac: ~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/

Nochtans, kan de plaats afhankelijk van het gevormde eindpunt van AEM Desktop veranderen AEM. De waarde is een gecodeerde versie van de beoogde URL. Als de toepassing zich bijvoorbeeld richt op `http://localhost:4502`de toepassing, is de mapnaam `http%3A%2F%2Flocalhost%3A4502%2F`.

Als u de cache wilt wissen, verwijdert u de map &lt;Encoded AEM Endpoint>.

>[!NOTE]
>
>Als u de AEM Desktop-cache wist, gaan lokale bestandswijzigingen die niet naar AEM worden gesynchroniseerd, verloren.

>[!NOTE]
>
>Vanaf versie 1.5 van de AEM-bureaubladtoepassing is er een optie in de interface van de bureaubladtoepassing om de cache te wissen.

## De AEM Desktop-versie zoeken {#finding-the-aem-desktop-version}

De procedure om de AEM Desktop versie te controleren is het zelfde voor zowel Vensters als MAC OS.

Klik op het pictogram AEM-bureaublad en kies vervolgens **Info**. Het versienummer wordt op het scherm weergegeven.

## AEM-bureaubladtoepassing upgraden op MacOS {#upgrading-aem-desktop-app-on-macos}

Soms kunnen er problemen optreden wanneer u de AEM-bureaubladtoepassing op MacOS upgradet. Dit wordt veroorzaakt door een oudere systeemmap voor de AEM-bureaubladtoepassing, waardoor nieuwe versies van AEM Desktop niet correct kunnen worden geladen. U kunt dit probleem verhelpen door de volgende mappen en bestanden handmatig te verwijderen.

Voordat u de onderstaande stappen uitvoert, sleept u de toepassing &quot;Adobe Experience Manager Desktop&quot; van de map MacOS-toepassingen naar de prullenmand. Open vervolgens de terminal en voer de volgende opdracht uit, waarbij u uw wachtwoord opgeeft wanneer hierom wordt gevraagd.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Een bestand opslaan dat door anderen is uitgecheckt {#saving-a-file-checked-out-by-others}

De technische beperkingen van het besturingssysteem verhinderen dat gebruikers een consistente ervaring hebben bij het overschrijven van een bestand dat door anderen is uitgecheckt. De ervaring varieert afhankelijk van de toepassing die wordt gebruikt om het uitgecheckte bestand te bewerken. Soms wordt in de toepassing een foutbericht weergegeven dat een schrijffout van een schijf aangeeft of dat een schijnbaar niet-verwante of algemene fout wordt weergegeven. In andere gevallen wordt geen foutbericht weergegeven en lijkt de bewerking te zijn geslaagd.

In dat geval kan bij het sluiten en opnieuw openen van het bestand blijken dat de inhoud ongewijzigd blijft. Sommige toepassingen kunnen echter een back-up van het bestand opslaan, zodat de wijzigingen kunnen worden toegepast.

Het bestand blijft ongewijzigd wanneer u het incheckt, ongeacht het gedrag. Zelfs als een andere versie van het bestand wordt weergegeven, worden de wijzigingen niet gesynchroniseerd met AEM.

## Problemen met het verplaatsen van bestanden oplossen {#troubleshooting-problems-around-moving-files}

De server-API vereist extra kopballen, x-Bestemming, x-Diepte, en x-Overschrijf, om worden overgegaan voor de beweging en exemplaarverrichtingen om te werken. De verzender geeft deze headers standaard niet door, waardoor deze bewerkingen mislukken. Zie [Verbinding maken met AEM achter een Dispatcher](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)voor meer informatie.

## Problemen met de AEM Desktop-verbinding oplossen {#troubleshooting-aem-desktop-connection-issues}

### SAML-omleiding {#saml-redirect-issue}

De gemeenschappelijkste reden voor kwesties met AEM Desktop die met uw SSO-Toegelaten (SAML) AEM instantie verbinden is dat het proces SAML niet naar de oorspronkelijk gevraagde weg opnieuw richt. De verbinding kan ook worden omgeleid naar een host die niet in een AEM-bureaublad is geconfigureerd. Voer de volgende stappen uit om het aanmeldingsproces te verifiëren:

1. Open een webbrowser.
1. Geef in de adresbalk de URL op `/content/dam.json`.
1. Vervang de URL bijvoorbeeld door de AEM-doelinstantie `http://localhost:4502/content/dam.json`.
1. Meld u aan bij AEM.
1. Controleer na het aanmelden het huidige adres van de browser in de adresbalk. Deze moet overeenkomen met de URL die u oorspronkelijk hebt ingevoerd.
1. Controleer of alles vóór de AEM-doelwaarde die in AEM Desktop is geconfigureerd, `/content/dam.json` overeenkomt.

### Probleem met SSL-configuratie {#ssl-configuration-issue}

De bibliotheken die AEM-bureaubladtoepassingen gebruiken voor HTTP-communicatie, maken gebruik van strikte SSL-afgedwongen omzetting. Soms kan een verbinding met een browser slagen, maar wordt de AEM-bureaubladtoepassing niet gebruikt. Installeer het ontbrekende tussentijdse certificaat in Apache om SSL op de juiste wijze te configureren. Zie [Een tussenpersoon installeren in Apache](https://access.redhat.com/solutions/43575).

## AEM Desktop gebruiken met dispatcher {#using-aem-desktop-with-dispatcher}

AEM Desktop werkt met AEM plaatsingen achter een verzender, die een gebrek en geadviseerde configuratie voor servers AEM is. AEM-verzenders vóór AEM-ontwerpomgevingen worden doorgaans geconfigureerd om DAM-elementen in cache over te slaan. Daarom bieden verzenders geen extra caching vanuit het standpunt van AEM Desktop. Zorg ervoor dat de configuratie van de verzender is aangepast aan de werking van AEM Desktop. Zie [Verbinding maken met AEM achter een verzender](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)voor meer informatie.

## Controleren op logbestanden {#checking-for-log-files}

Afhankelijk van uw besturingssysteem vindt u de logbestanden voor AEM Desktop op de volgende locaties:

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`
* Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`