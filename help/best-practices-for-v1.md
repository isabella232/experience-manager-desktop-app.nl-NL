---
title: Aanbevolen werkwijzen voor AEM-bureaubladtoepassing versie 1.x
description: Belangrijke mogelijkheden en aanbevolen gebruik van Adobe Experience Manager-bureaubladtoepassing versie 1.x.
uuid: ba8fbc74-e1ad-4085-a031-ffd317628ba6
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 57d5cd78-abce-4ede-a50e-7c161ddb43ae
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b92e47456f9e16c24eac43d1c5fef9a582f143b5

---


# Aanbevolen werkwijzen voor AEM-bureaubladtoepassing v1.x {#aem-desktop-app-best-practices}

## Overzicht {#overview}

De bureaubladtoepassing Adobe Experience Manager (AEM) koppelt de DAM-oplossing aan uw bureaublad, zodat u de bestanden die beschikbaar zijn in de AEM-webinterface rechtstreeks op het bureaublad kunt openen. Als u middelen van Desktop bewaart, wordt het geupload aan AEM bij de aangewezen plaats.

Met de AEM-bureaubladtoepassing voorkomt u dat u onjuiste lokale kopieën bijwerkt of een verkeerd middel bijwerkt in AEM. de gebruiksvriendelijke workflow van de bureaubladtoepassing wordt ingeschakeld met de technologie voor netwerkdeling die desktopbesturingssystemen bieden.

Desktop-app monteert de AEM Assets-opslagplaats als netwerkshare op desktop. Daarom worden de mappen en bestanden weergegeven alsof ze lokaal zijn. Het wordt echter afgeraden om bewerkingen voor het beheer van digitale elementen rechtstreeks vanaf het bureaublad uit te voeren in het gekoppelde netwerkaandeel in Finder of Explorer. In plaats daarvan raadt Adobe u aan de AEM Assets-webinterface te gebruiken voor het uitvoeren van bewerkingen, zoals het kopiëren of verplaatsen van een groot aantal elementen.

>[!NOTE]
>
>Voordat u dit document leest, kunt u de algemene best practices [voor](https://docs.adobe.com/content/help/en/experience-manager-64/assets/administer/aem-cc-integration-best-practices.html) AEM- en Creative Cloud-integratie doornemen voor een overzicht op een hoger niveau van het onderwerp.

## AEM-bureaubladtoepassingsarchitectuur {#aem-desktop-app-architecture}

De AEM-bureaubladtoepassing gebruikt WebDAV-netwerkshares (Windows) of SMB-netwerkshares (Mac) om netwerkshares te koppelen. Het gekoppelde netwerkaandeel is alleen lokaal. De AEM-bureaubladtoepassing onderschept de aanroepen (openen, lezen, schrijven) en biedt extra lokale caching. Het vertaalt verre vraag aan de server van Activa AEM aan geoptimaliseerde HTTP- verzoeken van AEM. Het volgende diagram toont de AEM desktop app architectuur.

![AEM-bureaubladtoepassingsarchitectuur](assets/chlimage_1.png)

Als een bestand wordt opgeslagen, wordt het bestand eerst lokaal opgeslagen (zodat de gebruiker niet op de netwerkoverdracht wacht) omdat het bestand tijdens het schrijven in cache wordt opgeslagen. Vervolgens wordt het bestand na een vooraf gedefinieerde vertraging (30 seconden) op de achtergrond geüpload naar AEM en wordt het element vervolgens geüpload naar AEM. De AEM-bureaubladtoepassing biedt een interface voor het controleren van de status van uploads van achtergrondbestanden.

## Aanbevolen gebruik van AEM-bureaubladtoepassing {#recommended-use-of-aem-desktop-app}

De belangrijkste mogelijkheden van de AEM-bureaubladtoepassing zijn:

* Bestanden openen vanuit de gebruikersinterface van AEM Assets op het bureaublad: Vanuit de webinterface kunt u middelen op het bureaublad (in Finder, Verkenner) weergeven of een element openen met een bureaubladtoepassing.
* Uitchecken en inchecken: Elementen kunnen worden uitgecheckt om te worden bewerkt. Ze zijn gemarkeerd als vergrendeld voor de gebruiker in AEM Assets. Na het bewerken kunt u het element inchecken om het te ontgrendelen.
* Wijzigingen in bestanden opslaan: Wijzigingen die u in het gedeelde netwerkbestand opslaat, worden automatisch naar AEM geüpload en er wordt een nieuwe versie gemaakt.
* Gekoppelde elementen in andere documenten plaatsen: In toepassingen zoals Creative Cloud (PS, ID, AI, enz.) kunt u een extern bestand als een koppeling plaatsen (u kunt bijvoorbeeld een afbeelding in een InDesign-document plaatsen). In dit geval kunt u met de netwerkshare-ount elementen van AEM zoeken en selecteren voor plaatsing. Het plaatsen van gekoppelde bestanden werkt ook in sommige niet-Adobe-toepassingen, zoals MS Office.
* Referentieresolutie in AEM: Als zowel het geplaatste bestand of de geplaatste bestanden als het hoofdbestand met de koppeling(en) in AEM zijn opgeslagen, kan het automatisch informatie geven over de elementen aan de serverzijde.
* Toegang tot middelen vanaf desktop: In het gekoppelde netwerkaandeel biedt een contextueel menu een dialoogvenster Meer informatie (grotere voorvertoning, belangrijke metagegevens) en de mogelijkheid om elementen te openen in de AEM-gebruikersinterface.
* Grote hiërarchische mappen bulksgewijs uploaden: Als u de optie Maken > Map uploaden in de AEM-gebruikersinterface gebruikt om elementen te uploaden, uploadt de AEM-bureaubladtoepassing de geselecteerde maphiërarchie naar AEM op de achtergrond. De voortgang van het uploaden kan worden gecontroleerd met een specifieke interface in de bureaubladtoepassing.

## Ongepast gebruik van AEM-bureaubladtoepassing {#inappropriate-use-of-aem-desktop-app}

* Gebruik de AEM-bureaubladtoepassing niet om elementen van het bureaublad te beheren. De AEM-bureaubladtoepassing is niet ontworpen als vervanging voor netwerkstations. Gebruik in plaats hiervan de volgende mogelijkheden:
   * AEM Assets-webinterface voor beheer van digitale elementen (zoeken/delen van elementen, metagegevens, kopiëren/verplaatsen, enz.)
   * AEM-bureaubladmap voor app uploaden om grote hiërarchische mappen te uploaden

* Behandel AEM-bureaubladtoepassing niet als een client voor desktopsynchronisatie voor AEM-middelen. Het belangrijkste voordeel van de AEM-bureaubladtoepassing hier is dat deze &#39;virtuele&#39; toegang biedt tot de gehele opslagruimte en dat toepassingen voor desktopsynchronisatie doorgaans slechts elementen van één gebruiker synchroniseren. De AEM-bureaubladtoepassing biedt enige mate van caching en uploaden naar de achtergrond. toch werkt het programma heel anders dan gewone &quot;Sync&quot;-toepassingen, zoals Adobe Creative Cloud-bureaubladtoepassing of Microsoft OneDrive.
* Gebruik geen netwerkstations van AEM-bureaubladapps om elementen regelmatig op te slaan. Alle opslagbewerkingen worden naar AEM Assets verzonden. Daarom is het onpraktisch om intensieve bewerkingen rechtstreeks uit te voeren in de gekoppelde AEM Assets-opslagplaats. Door een element rechtstreeks in de gekoppelde opslagplaats te bewerken, loopt de tijdlijn van het element vast met irrelevante versies en worden extra overheadkosten aan de server opgelegd.
* Gebruik de AEM-bureaubladtoepassing niet voor de migratie van grote hoeveelheden gegevens van de ene AEM-instantie naar de andere. Raadpleeg de [migratiehandleiding](https://docs.adobe.com/content/help/en/experience-manager-65/assets/administer/assets-migration-guide.html) om de migratie van middelen te plannen en uit te voeren. Desktop-app daarentegen [ondersteunt het uploaden](use-app-v1.md#bulkupload) van grote hoeveelheden middelen voor het eerst in AEM.

## Aanbevelingen voor geselecteerde gebruiksgevallen {#recommendations-for-selected-use-cases}

### Toegang tot middelen voor creatieve gebruikers {#access-to-assets-for-creative-users}

De AEM-bureaubladtoepassing biedt virtuele toegang tot de hele DAM-opslagplaats - en het kan lastig zijn voor creatieve gebruikers op desktopcomputers om de juiste middelen op hun bureaublad te vinden en te openen. Gebruik deze beste praktijken om dat voor hen te vereenvoudigen.

* Gebruik samenwerkingsfuncties in de gebruikersinterface van AEM Assets om de creatieve gebruiker directere toegang tot de juiste middelen te bieden. U kunt onder andere mappen of verzamelingen delen, slimme verzamelingen (opgeslagen zoekopdrachten) opgeven of meldingen met aanwijzers naar de juiste elementen verzenden. Creative gebruikers kunnen vervolgens bureaubladacties in de webinterface gebruiken om snel toegang tot deze middelen op hun bureaublad te krijgen.
* Overweeg de juiste machtigingen voor middelen (toegangsbeheer) om de weergave in de DAM-opslagplaats voor creatieve gebruikers te vereenvoudigen, zodat ze in feite alleen toegang hebben tot de middelen die ze nodig hebben of waarin ze geïnteresseerd zijn:

   * Bepaalde gebieden die niet relevant zijn voor de creatieve gebruikers kunnen worden geweigerd voor hun gebruikersgroep(en), om ze uit hun weergave te verwijderen, ook op het bureaublad
   * De meeste activa in DAM zijn definitief en niet bedoeld om te veranderen - deze zouden read-only voor de creatieve gebruikers moeten zijn
   * Alleen elementen die moeten worden gewijzigd/geretoucheerd, moeten voor creatieve gebruikers zijn ingeschakeld. Sommige organisaties gebruiken AEM Projecten en de omslagen zij creëren om activa te ontvangen die nog onderworpen aan veranderingen zijn.

### Elementen zoeken {#searching-assets}

Ga als volgt te werk om een bestand te zoeken dat u op het bureaublad wilt openen:

* Gebruik de interface van het AEM Assets-web om het element te zoeken. Niet alleen is het zoeken in AEM Middelen krachtig (onderzoeksfacetten, bewaarde onderzoeken), het verstrekt ook extra mogelijkheden om de juiste activa te vinden. Deze omvatten extra filters, zoals de capaciteit om activa te zoeken die op status (goedkeuring, vervaldatum) worden gebaseerd, inzamelingen, taken, berichten, en het delen van omslagen/inzamelingen met andere gebruikers/groepen.
* Nadat u het element hebt gevonden, gebruikt u Bureaubladhandelingen in de AEM-gebruikersinterface om het element op het bureaublad te openen.

### Elementen bijwerken die zijn geopend met de AEM-bureaubladtoepassing {#updating-assets-opened-using-aem-desktop-app}

Als u een middel direct op de plaats uitgeeft die van Middelen AEM aan een lokaal netwerkaandeel in kaart wordt gebracht, wordt het middel geupload aan AEM telkens als u het op Desktop bewaart. Daarnaast maakt AEM een versie en worden uitvoeringen gegenereerd.

Als een in AEM opgeslagen element een update nodig heeft:

* Voor **kleine updates**, zoals kleine retoucheringsverzoeken in het goedkeuringsproces:

   * Het bestand uitchecken en openen op het bureaublad
   * Het bestand bijwerken
   * Sla de bijgewerkte versie op. Het element wordt bijgewerkt en de tijdlijn geeft de oorspronkelijke versie weer ter vergelijking

* Voor **belangrijke updates**, zoals een veranderingsverzoek dat een kleine creatieve cyclus van WIP vereist:

   * Gebruik de optie Tonen om de juiste map op het bureaublad te openen
   * Kopieer het bestand naar een WIP-map buiten de toegewezen AEM Assets-share (kopieer het bestand bijvoorbeeld naar een map die is gesynchroniseerd met de Adobe Creative Cloud-bureaubladtoepassing)
   * Werk aan het bestand en sla het bestand af en toe op. De wijzigingen worden niet opgeslagen in AEM-elementen
   * Nadat de bewerkingen zijn voltooid, verplaatst, kopieert of slaat u het bestand dat van AEM is toegewezen, op om het te uploaden als een nieuwe versie

## Netwerkprestaties {#network-performance}

Een goede ervaring voor gebruikers die de AEM-bureaubladtoepassing gebruiken, is in hoge mate afhankelijk van goede, stabiele netwerkconnectiviteit tussen hun desktops en de AEM-server en van de server die is afgestemd op goede prestaties, met name bij het uploaden en bijwerken van middelen. Deze aanbevelingen zijn voor de netwerk/teams van IT in organisaties.

### Netwerkoverwegingen {#network-considerations}

Raadpleeg het document [AEM Assets Network Considerations (AEM Assets Network Overwegingen) voor](https://docs.adobe.com/content/help/en/experience-manager-64/assets/administer/assets-migration-guide.html) meer informatie over de beste werkwijzen met betrekking tot de netwerkconfiguratie van AEM Assets. Enkele belangrijke aspecten die de gebruikers helpen om de AEM-bureaubladervaring te optimaliseren, zijn onder andere:

* **Gebruik correct geconfigureerde Dispatcher:** AEM Dispatcher gebruiken voor extra beveiliging en zorgen dat deze is geconfigureerd voor [AEM-bureaubladtoepassingsverbinding met AEM achter een verzender](using.md)

* **Bandbreedte opslaan:** U kunt de voorvertoning van pictogrammen in Finder op Mac uitschakelen wanneer u in de gekoppelde opslagplaats bladert met Finder. Finder vraagt elk bestand om een voorvertoning te genereren en zorgt ervoor dat de bureaubladtoepassing het element lokaal downloadt en in cache plaatst. Houd er rekening mee dat als u bandbreedte bespaart, dit ook de gebruikerservaring voor gebruikers op het bureaublad vermindert, dus dat moet gebeuren als u werkt met opslagruimten met grote middelen en/of beperkte bandbreedte.

>[!NOTE]
>
>Als u pictogramvoorvertoningen wilt uitschakelen, gaat u in Finder naar Weergave, selecteert u Weergaveopties en schakelt u vervolgens de optie Pictogramvoorvertoning weergeven uit. Dit werkt alleen voor de huidige map. Klik op de knop &quot;Gebruiken als standaard&quot; in hetzelfde venster om van deze map een standaardmap te maken.

### Serverprestaties optimaliseren {#optimizing-server-performance}

Voor meer informatie over de manier waarop de AEM Assets-server geoptimaliseerd moet zijn voor prestaties, raadpleegt u de [AEM Assets Performance Tuning Guide](https://docs.adobe.com/content/help/en/experience-manager-65/assets/administer/performance-tuning-guidelines.html). Enkele belangrijke aspecten van de serverprestaties voor AEM-bureaubladtoepassingen zijn het optimaliseren van workflowconfiguratie, zodat deze goed functioneert bij het uploaden van middelen:

* **Verbeterde functionaliteit voor het uploaden van middelen:** Configureer het workflowmodel voor updates van [AEM-middelen zodat deze van voorbijgaande aard](https://docs.adobe.com/content/help/en/experience-manager-65/assets/administer/performance-tuning-guidelines.html#Workflows)zijn.

* **CPU voor uploads beperken:** Zorg ervoor dat de maximale parameter voor parallelle workflowtaken correct is ingesteld, zodat uploads niet alle CPU uitputten.
