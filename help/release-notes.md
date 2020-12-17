---
title: Opmerkingen bij de release Adobe Experience Manager-bureaubladtoepassing
description: Geef details, verbeteringen, nieuwe functies, compatibiliteit en downloadkoppelingen voor de Adobe Experience Manager-bureaubladtoepassing op.
uuid: b783c3f8-aa1e-4c05-b687-5894909769f5
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.5/ASSETS, SG_EXPERIENCEMANAGER/6.4/ASSETS, SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 3052549b-fe75-44fb-a55e-5cc612868f54
index: y
internal: n
snippet: y
mini-toc-levels: 1
translation-type: tm+mt
source-git-commit: 41625c59df00b82ceda8a566b35341bc51c2a30f
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---


# Opmerkingen bij de release Adobe Experience Manager-bureaubladtoepassing {#release-notes-v2}

| Producten | Adobe Experience Manager-bureaubladtoepassing |
|--- |--- |
| Toepassingsversie (revisie) | 2.1 (2.1.0.0) |
| Ondersteunde [!DNL Adobe Experience Manager] versies | [!DNL Experience Manager] als  [!DNL Cloud Service]een  [!DNL Experience Manager] 6.5.  [!DNL Experience Manager] 6.4.  [!DNL Experience Manager] 6.3 (met compatibiliteitspakket) |
| Type | Minder release |
| Releasedatum | 27 aug. 2020 (Mac en Windows) |
| URL&#39;s downloaden | [macOS 64-bits](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.0.0.dmg);  [Windows 64-bits](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.0.0.exe);  [Windows 32-bits](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.0.0.exe) |

## Systeemvereisten en -vereisten {#system-requirements-and-prerequisites-v2}

De Adobe Experience Manager-bureaubladtoepassing is compatibel met de volgende besturingssystemen:

* Mac OS X 10.14 of hoger, met de meest recente opgeloste problemen.

* Windows 10 met de recentste de dienstpakken en insectenmoeilijke situaties.

>[!NOTE]
>
>Windows 7 wordt niet meer ondersteund door de leverancier (https://support.microsoft.com/en-us/help/4057281/windows-7-support-ended-on-january-14-2020).

De app werkt met de volgende versies van Experience Managers, ongeacht of deze als Cloud Service zijn geïmplementeerd, op Adobe Managed Services (AMS) of op locatie:

* [[!DNL Experience Manager] als [!DNL Cloud Service]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/home.html) een.

* [[!DNL Experience Manager] 6.5.0](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html) of hoger.

* [[!DNL Experience Manager] 6.4.4](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html) of hoger.

* [!DNL Experience Manager] 6.4.0 - 6.4.3 met  [compatibiliteitspakket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support).

>[!NOTE]
>
>Ondersteuning voor bureaubladtoepassingen voor [!DNL Experience Manager] 6.3 is afgekeurd. Adobe raadt aan een upgrade naar een nieuwere en ondersteunde [!DNL Adobe Experience Manager]-versie uit te voeren.
>[!DNL Experience Manager] 6.3.3.1 of hoger werkt met een bureaubladtoepassing nadat het [compatibiliteitspakket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) is geïnstalleerd. Een dergelijk pakket is niet beschikbaar voor Experience Manager 6.3 omdat er geen [servicepacks zijn gepland](https://helpx.adobe.com/experience-manager/maintenance-releases-roadmap.html).

Voor de versie van de app die u op uw lokale computer wilt installeren, is een specifieke Adobe Experience Manager-serverversie/aanvullende serveronderdelen (servicepakketten, hotfixes of functiepakketten) vereist. Neem contact op met uw Adobe Experience Manager-beheerder voor hulp.

### Ondersteuning voor verschillende elementen en bestandstypen {#support-for-file-types}

De toepassing ondersteunt in Adobe Experience Manager opgeslagen elementen die binaire bestanden vertegenwoordigen voor basisbewerkingen. Het openen van bestanden in de oorspronkelijke bureaubladtoepassing is afhankelijk van de koppeling tussen het besturingssysteem van de specifieke bestandstypen, zoals PNG of JPG, en specifieke toepassingen, zoals Mac Preview of Adobe Photoshop.

Enkele bestandstypen ondersteunen het plaatsen van gekoppelde elementen in het binaire bestand. De toepassing downloadt de gekoppelde elementen vooraf als het element aanwezig is in de opslagplaats van de Experience Manager wanneer dergelijke binaire bestanden worden geopend met de bureaubladtoepassing. Momenteel worden de volgende bestandstypen ondersteund:

* [!DNL Adobe InDesign] bestanden (INDD-indeling)
* [!DNL Adobe Illustrator] bestanden (AI-indeling)
* [!DNL Adobe Photoshop] bestanden (PS-indeling)

De functie wordt ondersteund in Adobe Creative Cloud 2018- en Adobe Creative Cloud 2019-versies van de bovenstaande toepassing. De app gebruikt een heuristische, best-match benadering om de lokale Desktopwegen van verbonden activa aan URLs op de server van de Experience Manager in kaart te brengen. Het steunt op een paar veronderstellingen:

* Paden naar geplaatste bestanden in de oorspronkelijke toepassing gebruiken een globaal desktoppad (geplaatst vanuit het gedeelde lokale netwerk dat wordt weergegeven met de optie [!UICONTROL Reveal]).

* Paden worden door de native toepassing in de XMP record van het bestand opgeslagen.

* Experience Manager heeft de XMP-record geëxtraheerd met de paden naar de metagegevensrecord van het element.

* De paden kunnen worden aangepast aan elementen in Experience Manager, dat wil zeggen dat de geplaatste bestanden ook in Experience Manager zijn onder een overeenkomend pad.

## Nieuwe functies en verbeteringen {#whats-new-added}

Zie [Nieuwe functies in v2.0](introduction.md#whats-new-v2) voor meer informatie.

**Updates in app v2.1.0.0**

* Gebruikers kunnen nu bestanden of mappen op de interface van de toepassing slepen, rechtstreeks vanuit Windows Verkenner of de Finder. Dit werkt naast de uploadoptie die eerder beschikbaar was in de toepassing.

**Updates in app v2.0.3**

De bug die in de huidige versie is opgelost, is:

* Oplossing voor het aanmeldingsprobleem waarmee Windows-gebruikers via de app toegang probeerden te krijgen tot de DAM-opslagplaats op [!DNL Adobe Experience Manager] 6.5.5.0-exemplaar.

**Updates in app v2.0.2**

De opgeloste problemen en updates zijn:

* Verhoog de uploadversnelling in [!UICONTROL Preferences] om de uploadprestaties te verbeteren. Als deze instelling is ingeschakeld, gebruikt de app meer lokale CPU-threads en is de toepassing bronnenintensiever.

* Correctie van het probleem met het uploaden van middelen wanneer bestandsnamen of paden bepaalde GB18030-tekens bevatten. <!-- CQ-4283494 -->

* De optie Sorteren op relevantie is beschikbaar na het schakelen naar een ander type in de zoekresultaten. <!-- CQ-4286874 -->

* Desktop app geeft nu submappen weer zonder dat deze expliciet hoeven te worden vernieuwd. <!-- CQ-4285711 -->

* (Windows) Probleem met onbruikbare toepassingsinterface op sommige Windows-computers is opgelost. Gebruikers kunnen niet op de toepassingsinterface klikken omdat deze vervormd lijkt te zijn met het klikgebied van interface-elementen &#39;verschoven&#39; zijwaarts. <!-- CQ-4280785 -->

**Updates in app v2.0.1**

De opgeloste problemen en updates zijn:

* Optie toestaan om `%Temp%` directory zodanig te configureren dat deze overeenkomt met `%APPDATA%` pad. <!-- CQ-4282665 -->

* Gebruikers toestaan zich aan te melden bij Experience Manager Author via Okta SAML-verificatie. <!-- CQ-4278134 -->

## Installatie-instructies {#installation-instructions-v2}

Zie [Desktop app van Experience Manager installeren](install-upgrade.md) voor informatie over het installeren en configureren van de app.

Als u een upgrade uitvoert vanaf een eerdere Experience Manager-bureaubladtoepassing, moet u de volgende aanbevolen procedures voor overgangen volgen die worden vermeld bij [upgrade van vorige versie](install-upgrade.md#upgrade-from-previous-version).

## Belangrijke informatie over hoe de app werkt {#how-app-works}

Het is belangrijk om het volgende over de toepassing en hoe het werkt te begrijpen.

* De toepassing biedt volledige controle over bewerkingen waarvoor volledige overdracht van binaire elementen van en naar Experience Manager vereist is (bestanden openen, bewerken, uploaden en uploaden).

   * Als u met middelen op Desktop wilt werken, moet u uitdrukkelijk openen, uitgeven, of Download aan uw Desktop, of individueel, in een omslag, of via multi-selectie.

   * Als u lokale wijzigingen in naar Experience Manager geüploade elementen wilt ophalen, moet u [!UICONTROL Upload Changes] selecteren, afzonderlijk of via meerdere selecties.

   * De toepassing is geen &#39;synchronisatieclient&#39; die elementen synchroniseert op het bureaublad en de Experience Manager.

   * De toepassing biedt geen netwerkshare waarmee de gegevensopslagruimte van de Experience Manager wordt toegewezen als een virtuele mapstructuur.

* De lijst met elementen die door de toepassing wordt weergegeven, is gebaseerd op de status van de gegevensopslagplaats. Bestanden die lokaal zijn gedownload en waarvan de naam vervolgens is gewijzigd in de lokale bestanden of cachemap, worden niet weergegeven of beheerd door de toepassing.

* Als de app de verwachte resultaten niet weergeeft, klikt u op het pictogram Vernieuwen in de bovenste balk.

* Het lokale netwerkaandeel, dat wordt getoond wanneer u [!UICONTROL Reveal File] actie gebruikt, toont slechts dossiers (en omslagen) die plaatselijk beschikbaar zijn. [!UICONTROL Reveal File] en  [!UICONTROL Reveal Folder] vooraf downloadt middelen helpen de juiste activa krijgen die in het lokale netwerkaandeel tonen.

* Het lokale netwerkaandeel van SMB (MAC) /WebDAV (Win) wordt gebruikt wanneer een Adobe Creative Cloud-app de elementbestanden leest die zijn gekoppeld aan of geplaatst in een native bestand van de Creative Cloud-app.

In het volgende diagram ziet u de stroom van elementen en bestanden van de cloud naar het lokale bestandssysteem en andersom, zoals deze wordt geïnitieerd door gebruikersacties.

![Stroom van middelen van de server van de Experience Manager naar native bureaubladapps via bureaubladtoepassing](assets/da20_flow_diagram.png)

## Bekende problemen {#known-issues-v2}

**Problemen met de gebruikersinterface:**

* Soms wordt de interface van de bureaubladtoepassing leeg. Klik met de rechtermuisknop en klik op [!UICONTROL Refresh] om de toepassing opnieuw te laden. Nadat u deze vernieuwingen hebt aangebracht, begint u bij de basis van de DAM-opslagplaats. Updates of statussen van uw elementen blijven behouden. <!-- CQ-4270267 -->

* Kan moeilijk door mappen/zoekresultaten navigeren zonder trackpad of muisaanwijzer. De schuifbalk wordt mogelijk niet weergegeven met muisapparaten zonder muiswiel. <!-- CQ-4269947 -->

* De voortgangsbalk wordt soms niet correct weergegeven wanneer het uploaden van het element wordt gewijzigd.

* Nadat het filter is toegepast en verwijderd om alle lokaal bewerkte elementen te zoeken, leidt de app gebruikers niet naar hun zoekresultaten of mapweergave waarmee de gebruikers zijn gestart. De toepassing geeft de hoofdmap van de DAM-opslagplaats weer.

* Wanneer u verbinding maakt met een URL waarop geen Experience Manager-server wordt uitgevoerd, reageert het verbindingsscherm soms niet. Sluit de toepassing af en start deze opnieuw.

**Problemen met CRUD (maken, lezen, bijwerken en verwijderen):**

* Toepassing probeert bestanden te uploaden, zelfs met ongeldige tekens. Hierdoor kan uploadfout op de server optreden. <!-- CQ-4273652 -->

* Wanneer u wijzigingen in een element met opmerkingen uploadt, worden de opmerkingen met het element in de Experience Manager opgeslagen, maar zijn ze niet zichtbaar als versieopmerkingen. Dit probleem is opgelost in Experience Manager 6.4.5 en Experience Manager 6.5.1. Adobe raadt u ten zeerste aan de nieuwste servicepakketten te installeren. <!-- CQ-4268990 -->

* De overdracht van middelen kan niet door de gebruiker worden geannuleerd. Als u een onbedoelde grote overdracht hebt geactiveerd, sluit u de toepassing af en start u de toepassing opnieuw. <!-- CQ-4278940 -->

**Problemen met Platform:**

* Soms kan in Windows de status van een element direct veranderen in [!UICONTROL Edited Locally] nadat het is geopend, ook al hebt u het wellicht niet bewerkt. Klik [!UICONTROL Refresh] om bij te werken.

>[!MORELIKETHIS]
>
>* [Experience Manager als Cloud Service documentatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)
>* [Experience Manager als documentatie over Cloud Service Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html)
>* [Experience Manager desktop app gebruiken](using.md)
>* [Desktop-app installeren en upgraden](install-upgrade.md)
>* [Tips voor aanbevolen procedures en probleemoplossing](troubleshoot.md)

