---
title: Opmerkingen bij de release van Adobe Experience Manager-bureaublad
description: Geef details, verbeteringen, nieuwe functies, compatibiliteit en downloadkoppelingen op voor Adobe Experience Manager desktop app.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
mini-toc-levels: 1
translation-type: tm+mt
source-git-commit: 3eb9ab89ff6338fb29cfad1a031944119908d0a2
workflow-type: tm+mt
source-wordcount: '1320'
ht-degree: 3%

---


# Opmerkingen bij de release van Adobe Experience Manager-bureaublad {#release-notes-v2}

| Producten | Adobe Experience Manager-bureaubladtoepassing |
|--- |--- |
| Toepassingsversie (revisie) | 2.0 (2.0.2.0) |
| Ondersteunde AEM | AEM als Cloud Service; AEM 6.5; AEM 6.4; AEM 6.3 (met compatibiliteitspakket) |
| Type | Minder release |
| Releasedatum | 15 apr. 2020 (Mac en Windows) |
| URL&#39;s downloaden | [macOS 64-bits](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-osx-2.0.2.0.dmg); [Windows 64-bits](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win64-2.0.2.0.exe); [Windows 32-bits](https://download.macromedia.com/aem-assets-companion-app/aem-desktop-win32-2.0.2.0.exe) |

## Systeemvereisten en -vereisten {#system-requirements-and-prerequisites-v2}

De bureaubladtoepassing van de Adobe Experience Manager is compatibel met de volgende besturingssystemen:

* Mac OS X 10.14 of hoger, met de meest recente opgeloste problemen.

* Vensters 7 en Vensters 10 met de recentste de dienstpakken en insectenmoeilijke situaties.

De app werkt met de volgende versies van Experience Managers, ongeacht of deze als Cloud Service zijn geïmplementeerd, op Adobe Managed Services (AMS) of op locatie:

* [Experience Manager as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/home.html).

* [Experience Manager 6.5.0](https://docs.adobe.com/content/help/en/experience-manager-65/release-notes/release-notes.html) of hoger.

* [Experience Manager 6.4.4](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/release-notes.html) of hoger.

* Experience Manager 6.4.0 - 6.4.3 met [compatibiliteitspakket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support).

>[!NOTE]
>
>Ondersteuning voor bureaubladapps voor Experience Manager 6.3 is afgekeurd. Adobe raadt aan een upgrade uit te voeren naar een nieuwere en ondersteunde versie van de Adobe Experience Manager.
>Experience Manager 6.3.3.1 of hoger werkt na installatie van het [compatibiliteitspakket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)met de bureaubladtoepassing. Een dergelijk pakket is niet beschikbaar voor Experience Manager 6.3 omdat er geen [servicepacks zijn gepland](https://helpx.adobe.com/experience-manager/maintenance-releases-roadmap.html).

Voor de versie van de app die u op uw lokale computer wilt installeren, is een specifieke versie van de Adobe Experience Manager-server/aanvullende serveronderdelen (servicepacks, hotfixes of functiepakketten) vereist. Neem contact op met de beheerder van de Adobe Experience Manager voor hulp.

### Ondersteuning voor verschillende elementen en bestandstypen {#support-for-file-types}

De toepassing ondersteunt elementen die zijn opgeslagen in Adobe Experience Manager en die binair bestand vertegenwoordigen voor basisbewerkingen. Het openen van bestanden in de oorspronkelijke bureaubladtoepassing is afhankelijk van de koppeling tussen het besturingssysteem van de specifieke bestandstypen, zoals PNG of JPG, en specifieke toepassingen, zoals Mac Preview of Adobe Photoshop.

Enkele bestandstypen ondersteunen het plaatsen van gekoppelde elementen in het binaire bestand. De toepassing downloadt de gekoppelde elementen vooraf als het element aanwezig is in de opslagplaats van de Experience Manager wanneer dergelijke binaire bestanden worden geopend met de bureaubladtoepassing. Momenteel worden de volgende bestandstypen ondersteund:

* [!DNL Adobe InDesign] bestanden (INDD-indeling)
* [!DNL Adobe Illustrator] bestanden (AI-indeling)
* [!DNL Adobe Photoshop] bestanden (PS-indeling)

De functie wordt ondersteund in Adobe Creative Cloud 2018- en Adobe Creative Cloud 2019-versies van de bovenstaande toepassing. De app gebruikt een heuristische, best-match benadering om de lokale Desktopwegen van verbonden activa aan URLs op de server van de Experience Manager in kaart te brengen. Het steunt op een paar veronderstellingen:

* Paden naar geplaatste bestanden in de oorspronkelijke toepassing gebruiken een algemeen desktoppad (geplaatst vanuit het lokale netwerkaandeel dat met de [!UICONTROL Reveal] optie wordt weergegeven).

* Paden worden door de native toepassing in de XMP record van het bestand opgeslagen.

* Experience Manager heeft de XMP-record geëxtraheerd met de paden naar de metagegevensrecord van het element.

* De paden kunnen worden aangepast aan elementen in Experience Manager, dat wil zeggen dat de geplaatste bestanden ook in Experience Manager zijn onder een overeenkomend pad.

## Nieuwe en verbeterde functies {#whats-new-added}

Zie [Nieuwe functies in v2.0](introduction.md#whats-new-v2)voor meer informatie.

**Updates in app v2.0.2**

De opgeloste problemen en updates zijn:

* Verhoog de uploadversnelling in om de uploadprestaties te verbeteren [!UICONTROL Preferences]. Wanneer deze instelling is ingeschakeld, gebruikt de toepassing meer lokale CPU-threads en is de bronintensieve toepassing groter.

* Correctie van het probleem met het uploaden van middelen wanneer bestandsnamen of paden bepaalde GB18030-tekens bevatten. <!-- CQ-4283494 -->

* De optie Sorteren op relevantie is beschikbaar na het schakelen naar een ander type in de zoekresultaten. <!-- CQ-4286874 -->

* Desktop app geeft nu submappen weer zonder dat deze expliciet hoeven te worden vernieuwd. <!-- CQ-4285711 -->

* (Windows) Probleem met onbruikbare toepassingsinterface op sommige Windows-computers is opgelost. Gebruikers kunnen niet op de toepassingsinterface klikken omdat deze vervormd lijkt te zijn met het klikgebied van interface-elementen &#39;verschoven&#39; zijwaarts. <!-- CQ-4280785 -->

**Updates in app v2.0.1**

De opgeloste problemen en updates zijn:

* Optie toestaan om `%Temp%` directory zo te configureren dat deze overeenkomt met `%APPDATA%` pad. <!-- CQ-4282665 -->

* Gebruikers kunnen zich aanmelden bij AEM Author via Okta SAML-verificatie. <!-- CQ-4278134 -->

## Installatie-instructies {#installation-instructions-v2}

Zie Desktop-app [](install-upgrade.md)van Experience Manager installeren voor informatie over het installeren en configureren van de app.

Als u een upgrade uitvoert vanaf een eerdere Experience Manager-bureaubladtoepassing, moet u de volgende aanbevolen procedures voor overgangen volgen die worden weergegeven bij een [upgrade van de vorige versie](install-upgrade.md#upgrade-from-previous-version).

## Belangrijke informatie over hoe de app werkt {#how-app-works}

Het is belangrijk om het volgende over de toepassing en hoe het werkt te begrijpen.

* De toepassing biedt volledige controle over bewerkingen waarvoor de volledige overdracht van binaire elementen van en naar AEM vereist is (bestanden openen, bewerken, uploaden en uploaden).

   * Als u met middelen op Desktop wilt werken, moet u uitdrukkelijk openen, uitgeven, of Download aan uw Desktop, of individueel, in een omslag, of via multi-selectie.

   * Als u lokale wijzigingen in elementen wilt uploaden naar AEM, moet u deze afzonderlijk selecteren [!UICONTROL Upload Changes]of via meerdere selecties.

   * De toepassing is geen &#39;synchronisatieclient&#39; die elementen synchroniseert op het bureaublad en de AEM.

   * De toepassing biedt geen netwerkshare waarmee de AEM opslagplaats wordt toegewezen als een virtuele mapstructuur.

* De lijst met elementen die door de toepassing wordt weergegeven, is gebaseerd op de status van de gegevensopslagruimte van AEM Assets. Bestanden die lokaal zijn gedownload en waarvan de naam vervolgens is gewijzigd in de lokale bestanden of cachemap, worden niet weergegeven of beheerd door de toepassing.

* Als de app de verwachte resultaten niet weergeeft, klikt u op het pictogram Vernieuwen in de bovenste balk.

* Het lokale netwerkaandeel, dat wordt getoond wanneer u [!UICONTROL Reveal File] actie gebruikt, toont slechts dossiers (en omslagen) die plaatselijk beschikbaar zijn. [!UICONTROL Reveal File] en [!UICONTROL Reveal Folder] downloadt vooraf middelen helpen de juiste activa krijgen die in het lokale netwerkaandeel tonen.

* Het lokale netwerkaandeel van SMB (MAC) /WebDAV (Win) wordt gebruikt wanneer een Adobe Creative Cloud-app de elementbestanden leest die zijn gekoppeld aan of geplaatst in een native bestand van de Creative Cloud-app.

In het volgende diagram ziet u de stroom van elementen en bestanden van de cloud naar het lokale bestandssysteem en andersom, zoals deze wordt geïnitieerd door gebruikersacties.

![Stroom van middelen van AEM server naar native bureaubladapps via bureaubladtoepassing](assets/da20_flow_diagram.png)

## Known issues {#known-issues-v2}

**Problemen met de gebruikersinterface:**

* Soms wordt de interface van de bureaubladtoepassing leeg. Klik met de rechtermuisknop en klik [!UICONTROL Refresh] om de toepassing opnieuw te laden. Nadat u deze vernieuwingen hebt aangebracht, begint u bij de basis van de DAM-opslagplaats. Updates of statussen van uw elementen blijven behouden. <!-- CQ-4270267 -->

* Kan moeilijk door mappen/zoekresultaten navigeren zonder trackpad of muisaanwijzer. De schuifbalk wordt mogelijk niet weergegeven met muisapparaten zonder muiswiel. <!-- CQ-4269947 -->

* De voortgangsbalk wordt soms niet correct weergegeven wanneer het uploaden van het element wordt gewijzigd.

* Nadat het filter is toegepast en verwijderd om alle lokaal bewerkte elementen te zoeken, leidt de app gebruikers niet naar hun zoekresultaten of mapweergave waarmee de gebruikers zijn gestart. De toepassing geeft de hoofdmap van de DAM-opslagplaats weer.

* Als u verbinding maakt met een URL waarop AEM server niet wordt uitgevoerd, reageert het verbindingsscherm soms niet. Sluit de toepassing af en start deze opnieuw.

**Problemen met CRUD (maken, lezen, bijwerken en verwijderen):**

* Toepassing probeert bestanden te uploaden, zelfs met ongeldige tekens. Hierdoor kan uploadfout op de server optreden. <!-- CQ-4273652 -->

* Wanneer u wijzigingen in een element met opmerkingen uploadt, worden de opmerkingen met het element in AEM opgeslagen, maar zijn ze niet zichtbaar als opmerkingen bij de versieweergave. Dit probleem is opgelost in AEM 6.4.5 en AEM 6.5.1. Adobe raadt u ten zeerste aan de nieuwste servicepakketten te installeren. <!-- CQ-4268990 -->

* De overdracht van middelen kan niet door de gebruiker worden geannuleerd. Als u een onbedoelde grote overdracht hebt geactiveerd, sluit u de toepassing af en start u de toepassing opnieuw. <!-- CQ-4278940 -->

**Problemen met Platform:**

* Soms kan in Windows de status van een element direct veranderen in [!UICONTROL Edited Locally] nadat het is geopend, ook al hebt u het wellicht niet bewerkt. Klik [!UICONTROL Refresh] om bij te werken.

>[!MORELIKETHIS]
>
>* [AEM als documentatie voor Cloud Servicen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)
>* [AEM als documentatie bij Cloud Service Assets](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/home.html)
>* [Experience Manager desktop app gebruiken](using.md)
>* [Desktop-app installeren en upgraden](install-upgrade.md)
>* [Tips voor aanbevolen procedures en probleemoplossing](troubleshoot.md)

