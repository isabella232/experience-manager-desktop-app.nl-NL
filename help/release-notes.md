---
title: '[!DNL Adobe Experience Manager] Opmerkingen bij de release bureaubladapp'
description: Geen details, verbeteringen, nieuwe functies, compatibiliteit en downloadkoppelingen voor  [!DNL Adobe Experience Manager] desktop-app.
mini-toc-levels: 1
feature: Experience Manager Desktop-app, releasegegevens
translation-type: tm+mt
source-git-commit: 7204e3afb6d3a0908c076cf042072e3157572797
workflow-type: tm+mt
source-wordcount: '1474'
ht-degree: 0%

---


# [!DNL Adobe Experience Manager] Opmerkingen bij de release bureaubladapp  {#release-notes-v2}

De releasegegevens voor de nieuwste bureaubladtoepassing versie 2.1 (2.1.1.0) vindt u hieronder. De releasedatum is 5 maart 2021. Het is een kleine release met een verbetering.

De **ondersteunde [!DNL Experience Manager] versies** zijn:

* [!DNL Experience Manager] als een  [!DNL Cloud Service]. Zie [releaseopmerkingen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/home.html).
* [!DNL Experience Manager] 6.5.0 of hoger, op Adobe Managed Services (AMS) of op locatie. Zie [opmerkingen bij de release van het servicepack](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html).
* [!DNL Experience Manager] 6.4.4 of hoger, op Adobe Managed Services (AMS) of op locatie. Zie [opmerkingen bij de release van het servicepack](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html).
* [!DNL Experience Manager] 6.4.0 - 6.4.3 als het  [compatibiliteitspakket is ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) geïnstalleerd, op Adobe Managed Services (AMS) of op locatie.
* [!DNL Experience Manager] 6.3 (met compatibiliteitspakket)
* [!DNL Experience Manager] 6.3.3.1 of hoger als het  [compatibiliteitspakket is ](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) geïnstalleerd. Desktop-app wordt niet ondersteund voor [!DNL Experience Manager] 6.3.3.0 of eerdere versies.

[!DNL Adobe Experience Manager] bureaubladtoepassing is beschikbaar voor de volgende  **besturingssystemen**:

* macOS X 10.14 of hoger, met de nieuwste opgeloste problemen.
* Windows 10 met de recentste de dienstpakken en insectenmoeilijke situaties.

De **download URL&#39;s** voor ondersteund besturingssysteem zijn:

| Besturingssysteem | [!DNL Experience Manager] als  [!DNL Cloud Service] | [!DNL Experience Manager] 6,x |
|---|---|---|
| macOS 64-bits | [Koppeling downloaden](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.1.0.dmg) | [Koppeling downloaden](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.1.0.dmg) |
| Windows 64-bits | [Koppeling downloaden](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.1.0.exe) | [Koppeling downloaden](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.1.0.exe) |
| Windows 32-bits | [Koppeling downloaden](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.1.0.exe) | [Koppeling downloaden](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.1.0.exe) |

>[!NOTE]
>
>Windows 7 wordt niet meer ondersteund. Zie [het artikel over EOL van Vensters 7](https://support.microsoft.com/en-us/help/4057281/windows-7-support-ended-on-january-14-2020).

<!-- The version of the app you plan to install on your local machine requires a specific [!DNL Adobe Experience Manager] server version/additional server-side components (service packs, hot fixes, or feature packs). Contact your [!DNL Experience Manager] administrator for help.
-->

## Ondersteuning voor verschillende elementen en bestandstypen {#support-for-file-types}

De toepassing ondersteunt elementen die zijn opgeslagen in [!DNL Experience Manager] en die binair bestand vertegenwoordigen voor basisbewerkingen. Het openen van bestanden in de oorspronkelijke bureaubladtoepassing is afhankelijk van de koppeling tussen het besturingssysteem van de specifieke bestandstypen, zoals PNG of JPG, en specifieke toepassingen, zoals Mac Preview of Adobe Photoshop.

Enkele bestandstypen ondersteunen het plaatsen van gekoppelde elementen in het binaire bestand. De toepassing downloadt de gekoppelde elementen vooraf als het element aanwezig is in de [!DNL Experience Manager]-opslagruimte wanneer dergelijke binaire bestanden worden geopend met de bureaubladtoepassing. Momenteel worden de volgende bestandstypen ondersteund:

* [!DNL Adobe InDesign] bestanden (INDD-indeling)
* [!DNL Adobe Illustrator] bestanden (AI-indeling)
* [!DNL Adobe Photoshop] bestanden (PS-indeling)

De functie wordt ondersteund in de bovenstaande toepassing met [!DNL Adobe Creative Cloud] 2018- en [!DNL Adobe Creative Cloud] 2019-versies. De app gebruikt een heuristische, best-match benadering om de lokale Desktopwegen van verbonden activa aan URLs op de [!DNL Experience Manager] server in kaart te brengen. Het steunt op een paar veronderstellingen:

* Paden naar geplaatste bestanden in de oorspronkelijke toepassing gebruiken een globaal desktoppad (geplaatst vanuit het gedeelde lokale netwerk dat wordt weergegeven met de optie [!UICONTROL Reveal]).

* Paden worden door de native toepassing in de XMP record van het bestand opgeslagen.

* [!DNL Experience Manager] heeft de XMP record geëxtraheerd met de paden naar de metagegevensrecord van het element.

* De paden kunnen worden aangepast aan elementen in [!DNL Experience Manager], dat wil zeggen dat de geplaatste bestanden zich ook in [!DNL Experience Manager] onder een overeenkomend pad bevinden.

## Nieuwe functies, verbeteringen en foutoplossingen {#what-is-new}

Zie [Nieuwe functies in v2.0](introduction.md#whats-new-v2) voor meer informatie.

**Bijwerken in app v2.1.1.0**

* Met een geavanceerde instelling kan de toepassing het gedrag van de v1.10-app emuleren bij het uploaden van mappen. In v1.10, respecteren de knoopnamen die in de bewaarplaats worden gecreeerd ruimten en het omhulsel van de omslagnamen die door de gebruiker worden verstrekt. Het standaardgedrag van v2.1 blijft hetzelfde, dat wil zeggen: vervang meerdere spaties in mapnamen door een koppelteken in de naam van de opslagplaats en zet deze om in namen van kleine letters. Zie [de toepassingsvoorkeuren](/help/install-upgrade.md#set-preferences).

**Bijwerken in app v2.1.0.0**

* Gebruikers kunnen nu bestanden of mappen op de interface van de toepassing slepen, rechtstreeks vanuit Windows Verkenner of de Finder. Dit werkt naast de uploadoptie die eerder beschikbaar was in de toepassing. <!-- CQ-4309527 -->

**Bijwerken in app v2.0.3**

De bug die in de huidige versie is opgelost, is:

* Oplossing voor het aanmeldingsprobleem voor app-gebruikers in Windows die op [!DNL Adobe Experience Manager] 6.5.5.0 toegang proberen te krijgen tot de DAM-opslagplaats.

**Updates in app v2.0.2**

De opgeloste problemen en updates zijn:

* De instelling voor uploadversnelling is nu beschikbaar om de uploadprestaties te verbeteren. Als deze instelling is ingeschakeld, wordt de app sneller geüpload met meer lokale CPU-threads en is de toepassing bronnenintensiever.

* Het element wordt geüpload wanneer de bestandsnamen of paden die bepaalde GB18030-tekens bevatten, vast zijn. <!-- CQ-4283494 -->

* De optie Sorteren op relevantie is beschikbaar na het schakelen naar een ander type in de zoekresultaten. <!-- CQ-4286874 -->

* Desktop app geeft nu submappen weer zonder dat deze expliciet hoeven te worden vernieuwd. <!-- CQ-4285711 -->

* (Windows) Probleem met onbruikbare toepassingsinterface op sommige Windows-computers is opgelost. Gebruikers kunnen niet op de toepassingsinterface klikken omdat deze vervormd lijkt te zijn met het klikgebied van interface-elementen &#39;verschoven&#39; zijwaarts. <!-- CQ-4280785 -->

**Updates in app v2.0.1**

De opgeloste problemen en updates zijn:

* Optie toestaan om `%Temp%` directory zodanig te configureren dat deze overeenkomt met `%APPDATA%` pad. <!-- CQ-4282665 -->

* Gebruikers toestaan zich aan te melden bij [!DNL Experience Manager] Auteur via Okta SAML-verificatie. <!-- CQ-4278134 -->

## Installatie-instructies {#installation-instructions-v2}

Zie [Installeer [!DNL Experience Manager] Desktop app](install-upgrade.md) voor informatie over het installeren en configureren van de app.

Als u een upgrade uitvoert van een eerdere [!DNL Experience Manager]-bureaubladtoepassing, moet u de volgende aanbevolen procedures voor overgangen volgen die worden weergegeven bij [upgrade van vorige versie](install-upgrade.md#upgrade-from-previous-version).

## Belangrijke informatie over hoe de app werkt {#how-app-works}

Het is belangrijk om het volgende over de toepassing en hoe het werkt te begrijpen.

* De toepassing biedt volledige controle over bewerkingen waarvoor de volledige overdracht van binaire elementen van en naar [!DNL Experience Manager] vereist is (bestanden openen, bewerken, uploaden en uploaden).

   * Als u met middelen op Desktop wilt werken, moet u uitdrukkelijk openen, uitgeven, of Download aan uw Desktop, of individueel, in een omslag, of via multi-selectie.

   * Als u lokale wijzigingen in elementen wilt uploaden naar [!DNL Experience Manager], moet u [!UICONTROL Upload Changes] selecteren, afzonderlijk of via multiselectie.

   * De toepassing is geen &#39;synchronisatieclient&#39; die elementen synchroniseert op het bureaublad en [!DNL Experience Manager].

   * De toepassing biedt geen netwerkshare waarmee de [!DNL Experience Manager]-opslagplaats wordt toegewezen als een virtuele mapstructuur.

* De lijst met elementen die door de toepassing wordt weergegeven, is gebaseerd op de status van de gegevensopslagplaats. Bestanden die lokaal zijn gedownload en waarvan de naam vervolgens is gewijzigd in de lokale bestanden of cachemap, worden niet weergegeven of beheerd door de toepassing.

* Als de app de verwachte resultaten niet weergeeft, klikt u op het pictogram Vernieuwen in de bovenste balk.

* Het lokale netwerkaandeel, dat wordt getoond wanneer u [!UICONTROL Reveal File] actie gebruikt, toont slechts dossiers (en omslagen) die plaatselijk beschikbaar zijn. [!UICONTROL Reveal File] en  [!UICONTROL Reveal Folder] vooraf downloadt middelen helpen de juiste activa krijgen die in het lokale netwerkaandeel tonen.

* Het lokale netwerkaandeel van SMB (MAC) /WebDAV (Win) wordt gebruikt wanneer een Adobe Creative Cloud-app de elementbestanden leest die zijn gekoppeld aan of geplaatst in een native bestand van de Creative Cloud-app.

Het volgende diagram illustreert de stroom van elementen en bestanden van de cloud naar het lokale bestandssysteem en de omgekeerde manier, zoals wordt geïnitieerd door gebruikershandelingen.

![Stroom van middelen van de  [!DNL Experience Manager] server naar native bureaubladapps via bureaubladtoepassing](assets/da20_flow_diagram.png)

## Bekende problemen {#known-issues-v2}

**Problemen met de gebruikersinterface:**

* Soms wordt de interface van de bureaubladtoepassing leeg. Klik met de rechtermuisknop en klik op [!UICONTROL Refresh] om de toepassing opnieuw te laden. Nadat u deze vernieuwingen hebt aangebracht, begint u bij de basis van de DAM-opslagplaats. Updates of statussen van uw elementen blijven behouden. <!-- CQ-4270267 -->

* Kan moeilijk door mappen/zoekresultaten navigeren zonder trackpad of muisaanwijzer. De schuifbalk wordt mogelijk niet weergegeven met muisapparaten zonder muiswiel. <!-- CQ-4269947 -->

* De voortgangsbalk wordt soms niet correct weergegeven wanneer het uploaden van het element wordt gewijzigd.

* Nadat het filter is toegepast en verwijderd om alle lokaal bewerkte elementen te zoeken, leidt de app gebruikers niet naar hun zoekresultaten of mapweergave waarmee de gebruikers zijn gestart. De toepassing geeft de hoofdmap van de DAM-opslagplaats weer.

* Als u verbinding maakt met een URL waarop [!DNL Experience Manager] geen server actief is, reageert het verbindingsscherm soms niet. Sluit de toepassing af en start deze opnieuw.

**Problemen met CRUD (maken, lezen, bijwerken en verwijderen):**

* Toepassing probeert bestanden te uploaden, zelfs met ongeldige tekens. Hierdoor kan uploadfout op de server optreden. <!-- CQ-4273652 -->

* Wanneer u wijzigingen in een element met opmerkingen uploadt, worden de opmerkingen met het element opgeslagen in [!DNL Experience Manager], maar zijn ze niet zichtbaar als versieopmerkingen. Dit probleem is opgelost in [!DNL Experience Manager] 6.4.5 en [!DNL Experience Manager] 6.5.1. Adobe raadt u aan de nieuwste servicepakketten te installeren. <!-- CQ-4268990 -->

* De overdracht van middelen kan niet door de gebruiker worden geannuleerd. Als u een onbedoelde grote overdracht hebt geactiveerd, sluit u de toepassing af en start u de toepassing opnieuw. <!-- CQ-4278940 -->

**Problemen met Platform:**

* Soms kan in Windows de status van een element direct veranderen in [!UICONTROL Edited Locally] nadat het is geopend, ook al hebt u het wellicht niet bewerkt. Klik [!UICONTROL Refresh] om bij te werken.

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] documentatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] [!DNL Assets] documentatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html)
>* [Bureaubladapp  [!DNL Experience Manager] gebruiken](using.md)
>* [Desktop-app installeren en upgraden](install-upgrade.md)
>* [Tips voor aanbevolen procedures en probleemoplossing](troubleshoot.md)

