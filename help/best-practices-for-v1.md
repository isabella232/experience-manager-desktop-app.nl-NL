---
title: Aanbevolen werkwijzen voor bureaubladtoepassing v1.10
description: Belangrijkste mogelijkheden en aanbevolen gebruik van [!DNL Adobe Experience Manager] bureaubladtoepassing versie 1.10.
exl-id: 5de06b33-c05c-47eb-b884-408b6f9afc94
source-git-commit: 7a7236c36f615e97e9d040e6139368a931eb579e
workflow-type: tm+mt
source-wordcount: '1676'
ht-degree: 0%

---

# Aanbevolen werkwijzen AEM desktop app v1.10 {#aem-desktop-app-best-practices}

## Overzicht {#overview}

[!DNL Adobe Experience Manager] de bureaubladtoepassing koppelt uw DAM-oplossing (Digital Asset Management) aan uw bureaublad, zodat u de bestanden die beschikbaar zijn in de AEM webinterface rechtstreeks op uw bureaublad kunt openen. Als u middelen van Desktop bewaart, wordt het geupload aan AEM bij de aangewezen plaats.

AEM desktop app voorkomt dat u onjuiste lokale kopieën bijwerkt of een verkeerd middel in AEM bijwerkt. de gebruiksvriendelijke workflow van de bureaubladtoepassing wordt ingeschakeld met de technologie voor netwerkdeling die desktopbesturingssystemen bieden.

Desktop app monteert de AEM Assets-opslagplaats als netwerkshare op desktop. Daarom worden de mappen en bestanden weergegeven alsof ze lokaal zijn. Het wordt echter afgeraden om bewerkingen voor het beheer van digitale elementen rechtstreeks vanaf het bureaublad uit te voeren in het gekoppelde netwerkaandeel in Finder of Explorer. In plaats daarvan raadt Adobe u aan de gebruikersinterface van AEM Assets te gebruiken om bewerkingen uit te voeren, zoals het kopiëren of verplaatsen van een groot aantal elementen.

>[!NOTE]
>
>Voordat u dit document leest, kunt u de algemene [Aanbevolen werkwijzen voor integratie met AEM en Creative Cloud](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/aem-cc-integration-best-practices.html) voor een overzicht op hoger niveau van het onderwerp.

## AEM bureaubladtoepassingsarchitectuur {#aem-desktop-app-architecture}

AEM desktop gebruikt WebDAV (Windows) of SMB (Mac) netwerkshares om netwerkshares te koppelen. Het gekoppelde netwerkaandeel is alleen lokaal. AEM bureaubladtoepassing onderschept de aanroepen (openen, lezen, schrijven) en biedt extra lokale caching. Het vertaalt verre vraag aan de server van AEM Assets aan geoptimaliseerde AEM HTTP- verzoeken. In het volgende diagram wordt de architectuur van de AEM desktop-app weergegeven.

![AEM bureaubladtoepassingsarchitectuur](assets/arch_v1.png)

*Afbeelding: bureaubladtoepassingsarchitectuur*

Als een bestand wordt opgeslagen, wordt het bestand eerst lokaal opgeslagen (zodat de gebruiker niet op de netwerkoverdracht wacht) omdat het bestand tijdens het schrijven in cache wordt opgeslagen. Na een vooraf gedefinieerde vertraging (30 seconden) wordt het bestand geüpload naar AEM op de achtergrond en wordt het element vervolgens geüpload naar AEM. AEM bureaubladtoepassing biedt een interface voor het controleren van de status van uploads van achtergrondbestanden.

## Aanbevolen gebruik van AEM bureaubladtoepassing {#recommended-use-of-aem-desktop-app}

De belangrijkste mogelijkheden van AEM bureaubladtoepassing zijn:

* **Bestanden openen vanuit de gebruikersinterface van AEM Assets Web op het bureaublad**. Vanuit de webinterface kunt u middelen op het bureaublad (in Finder, Verkenner) weergeven of een element openen met een bureaubladtoepassing.

* **Uitchecken en inchecken**. Elementen kunnen worden uitgecheckt om te worden bewerkt. Ze zijn gemarkeerd als vergrendeld voor de gebruiker in AEM Assets. Na het bewerken kunt u het element inchecken om het te ontgrendelen.

* **Wijzigingen in bestanden opslaan**. Wijzigingen die u in het gedeelde netwerkbestand opslaat, worden automatisch naar AEM geüpload en er wordt een nieuwe versie gemaakt.

* **Gekoppelde elementen in andere documenten plaatsen**. In toepassingen, zoals Creative Cloud ([!DNL Adobe Photoshop], [!DNL Adobe InDesign], en [!DNL Adobe Illustrator]), kunt u een extern bestand als een koppeling plaatsen. U kunt bijvoorbeeld een afbeelding in een InDesign-document plaatsen. In dit geval kunt u met de netwerkshare-ount elementen van AEM selecteren en zoeken naar plaatsing. Het plaatsen van gekoppelde bestanden werkt ook in sommige apps die geen Adobe zijn, zoals MS Office.

* **Referentieresolutie in AEM**. Als zowel de geplaatste bestanden als de hoofdbestanden met de koppeling zijn opgeslagen in AEM, kan dit automatisch informatie geven over de elementen die naar de server worden verwezen.

* **Toegang tot het element vanaf het bureaublad**. In het gekoppelde netwerkaandeel biedt een contextueel menu een [!UICONTROL More Info] (grotere voorvertoning, belangrijke metagegevens) en de mogelijkheid om elementen te openen in de AEM-interface.

* **Grote, hiërarchische mappen bulksgewijs uploaden**. Als u de optie Maken > Map uploaden in AEM gebruikersinterface gebruikt om elementen te uploaden, uploadt AEM bureaubladtoepassing de geselecteerde maphiërarchie naar AEM op de achtergrond. De voortgang van het uploaden kan worden gecontroleerd met een specifieke interface in de bureaubladtoepassing.

## Ongepast gebruik van AEM bureaubladtoepassing {#inappropriate-use-of-aem-desktop-app}

* Gebruik AEM bureaubladtoepassing niet om elementen van het bureaublad te beheren. AEM bureaubladtoepassing is niet ontworpen als vervanging voor netwerkstations. Gebruik in plaats hiervan de volgende mogelijkheden:

   * AEM Assets-webinterface voor beheer van digitale elementen (zoeken naar of delen van elementen, metagegevens en kopiëren of verplaatsen).

   * Bureaubladapp AEM [!UICONTROL Folder Upload] om grote, hiërarchische mappen te uploaden.

* Behandel AEM bureaubladtoepassing niet als een &quot;desktop sync&quot;-client voor AEM Assets. Het belangrijkste voordeel van AEM bureaubladtoepassing is dat deze &#39;virtuele&#39; toegang biedt tot de gehele opslagruimte en dat toepassingen voor desktopsynchronisatie doorgaans alleen elementen synchroniseren die bij één gebruiker horen. AEM desktop-app biedt enige mate van caching en uploaden naar de achtergrond; toch werkt het heel anders dan bij gangbare &quot;Sync&quot;-toepassingen, zoals Adobe Creative Cloud-bureaubladtoepassingen of Microsoft OneDrive.

* Gebruik AEM netwerkstations voor bureaubladtoepassingen niet om elementen vaak op te slaan. Alle opslagbewerkingen worden naar AEM Assets verzonden. Daarom is het onpraktisch om intensieve bewerkingen rechtstreeks uit te voeren in de gekoppelde AEM Assets-opslagplaats. Door een element rechtstreeks in de gekoppelde opslagplaats te bewerken, loopt de tijdlijn van het element vast met irrelevante versies en worden extra overheadkosten aan de server opgelegd.

* Gebruik AEM bureaubladtoepassing niet voor het migreren van grote hoeveelheden gegevens van de ene AEM naar de andere. Zie de [Migratiehandleiding](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/assets-migration-guide.html) om migratie van middelen te plannen en uit te voeren. Desktop-app daarentegen [ondersteunt bulkuploaden](use-app-v1.md#bulkupload) groot aantal activa voor het eerst in [!DNL Adobe Experience Manager].

## Recommendations voor geselecteerde gebruiksgevallen {#recommendations-for-selected-use-cases}

### Toegang tot middelen voor creatieve gebruikers {#access-to-assets-for-creative-users}

AEM bureaubladtoepassing biedt virtuele toegang tot de hele DAM-opslagplaats - en het kan lastig zijn voor creatieve gebruikers op desktopcomputers om de juiste middelen op hun bureaublad te vinden en te openen. Gebruik deze beste praktijken om dat voor hen te vereenvoudigen.

* De samenwerkingseigenschappen van het gebruik in de UI van het Web van AEM Assets om directere toegang tot de juiste activa voor de creatieve gebruiker te verlenen. U kunt onder andere mappen of verzamelingen delen, slimme verzamelingen (opgeslagen zoekopdrachten) opgeven of meldingen met aanwijzers naar de juiste elementen verzenden. Creative gebruikers kunnen vervolgens bureaubladacties in de webinterface gebruiken om snel toegang tot deze middelen op hun bureaublad te krijgen.

* Overweeg de juiste machtigingen voor middelen (toegangsbeheer) om de weergave in de DAM-opslagplaats voor creatieve gebruikers te vereenvoudigen, zodat ze in feite alleen toegang hebben tot de middelen die ze nodig hebben of waarin ze geïnteresseerd zijn:

   * Bepaalde gebieden die niet relevant zijn voor de creatieve gebruikers kunnen worden geweigerd voor hun gebruikersgroepen, om ze uit hun weergave te verwijderen, ook op het bureaublad.

   * De meeste middelen in DAM zijn definitief en zijn niet bedoeld om te worden gewijzigd. Deze dienen alleen-lezen te zijn voor creatieve gebruikers.

   * Alleen elementen die moeten worden gewijzigd of geretoucheerd, moeten voor creatieve gebruikers zijn ingeschakeld. Sommige organisaties gebruiken AEM Projecten en de omslagen die zij aan gastheeractiva creëren die nog onderworpen aan veranderingen zijn.

### Elementen zoeken {#searching-assets}

Ga als volgt te werk om een bestand te zoeken dat u op het bureaublad wilt openen:

* Gebruik de AEM Assets-webinterface om het element te zoeken. Niet alleen is zoekopdracht in AEM Assets krachtig (zoekfacetten, opgeslagen zoekopdrachten), het biedt ook extra mogelijkheden om de juiste middelen te vinden. Deze omvatten extra filters, zoals de capaciteit om activa te zoeken die op status (goedkeuring, vervaldatum) worden gebaseerd, inzamelingen, taken, berichten, en het delen van omslagen/inzamelingen met andere gebruikers/groepen.

* Nadat u het element hebt gevonden, gebruikt u Bureaubladhandelingen in AEM gebruikersinterface om het element op het bureaublad te openen.

### Elementen bijwerken die zijn geopend met AEM bureaubladtoepassing {#updating-assets-opened-using-aem-desktop-app}

Als u een middel direct op de plaats uitgeeft die van AEM Assets aan een lokaal netwerkaandeel in kaart wordt gebracht, wordt het middel geupload aan AEM telkens als u het op Desktop bewaart. AEM maakt bovendien een versie en genereert uitvoeringen.

Als een in AEM opgeslagen element een update nodig heeft:

* Voor **kleine updates**, zoals kleine retoucheringsverzoeken in het kader van het goedkeuringsproces:

   * Check het bestand uit en open het op het bureaublad.

   * Werk het bestand bij.

   * Sla de bijgewerkte versie op. Het element wordt bijgewerkt en de tijdlijn geeft de oorspronkelijke versie weer ter vergelijking.

* Voor **belangrijke updates**, zoals een wijzigingsverzoek waarvoor een kleine creatieve WIP-cyclus is vereist:

   * Gebruik de optie Tonen om de juiste map op het bureaublad te openen.

   * Kopieer het bestand naar een WIP-map buiten de toegewezen AEM Assets-share (kopieer het bestand bijvoorbeeld naar een map die is gesynchroniseerd met de Adobe Creative Cloud-bureaubladtoepassing).

   * Werk aan het bestand en sla het bestand af en toe op. De wijzigingen worden niet opgeslagen in AEM Assets.

   * Nadat de bewerkingen zijn voltooid, verplaatst, kopieert of slaat u het bestand dat van AEM is toegewezen, op om het te uploaden als een nieuwe versie.

## Netwerkprestaties {#network-performance}

Een goede ervaring voor gebruikers die de AEM desktop-app gebruiken, is in hoge mate afhankelijk van goede, stabiele netwerkconnectiviteit tussen hun desktops en de AEM-server, en van de server die is afgestemd op goede prestaties, vooral bij het uploaden en bijwerken van middelen. Deze aanbevelingen zijn voor de netwerk/teams van IT in organisaties.

### Netwerkoverwegingen {#network-considerations}

Om beste praktijken rond de het netwerkconfiguratie van AEM Assets te begrijpen, gelieve te verwijzen naar [Hoe te om activa in bulk te migreren](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/assets-migration-guide.html) document. Enkele belangrijke aspecten die u helpen AEM bureaubladervaring voor de gebruikers te optimaliseren, zijn:

* **Gebruik correct geconfigureerde Dispatcher**. AEM Dispatcher gebruiken voor extra beveiliging en ervoor zorgen dat deze is geconfigureerd voor [Verbinding met bureaublad-app AEM naar AEM achter een dispatcher](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)

* **Bandbreedte opslaan**. U kunt pictogramvoorvertoning in Finder op Mac uitschakelen - wanneer u in de gekoppelde opslagplaats bladert met Finder. Finder vraagt elk bestand om een voorvertoning te genereren en zorgt ervoor dat de bureaubladtoepassing het element lokaal downloadt en in cache plaatst. Houd er rekening mee dat als u bandbreedte bespaart, dit ook de gebruikerservaring voor gebruikers op het bureaublad vermindert, dus dat moet gebeuren als u werkt met opslagruimten met grote middelen en/of beperkte bandbreedte.

>[!NOTE]
>
>Ga in Finder naar [!UICONTROL View], selecteert u [!UICONTROL View Options]en schakel vervolgens de optie [!UICONTROL Show icon preview] optie. Dit werkt alleen voor de huidige map. Klik op de knop [!UICONTROL Use as default] in hetzelfde dialoogvenster.

### Serverprestaties optimaliseren {#optimizing-server-performance}

Als u wilt weten hoe de AEM Assets-server moet worden geoptimaliseerd voor prestaties, raadpleegt u [AEM Assets Performance Tuning Guide](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/performance-tuning-guidelines.html). Sommige belangrijke aspecten van de serverprestaties voor AEM bureaubladtoepassing betreffen het optimaliseren van de workflowconfiguratie, zodat deze goed functioneert bij het uploaden van middelen:

* **Verbeterde functionaliteit voor uploaden van middelen**. Configureer de [Workflowmodel voor bijwerken van bedrijfsmiddelen AEM om van voorbijgaande aard te zijn](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/performance-tuning-guidelines.html).

* **CPU voor uploads beperken**. Zorg ervoor dat de maximale parameter voor parallelle workflowtaken correct is ingesteld, zodat uploads niet alle CPU uitputten.
