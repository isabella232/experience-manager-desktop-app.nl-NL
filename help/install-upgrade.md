---
title: Desktop-app installeren en configureren
description: Installeer en configureer  [!DNL Adobe Experience Manager] desktop app to work with [!DNL Adobe Experience Manager Assets] servers en download de middelen op uw lokale bestandssysteem.
feature: Experience Manager Desktop-app, releasegegevens
translation-type: tm+mt
source-git-commit: 7204e3afb6d3a0908c076cf042072e3157572797
workflow-type: tm+mt
source-wordcount: '1405'
ht-degree: 0%

---


# [!DNL Adobe Experience Manager] desktop app {#install-app-v2} installeren

Met de [!DNL Adobe Experience Manager]-bureaubladtoepassing zijn de middelen in [!DNL Experience Manager] eenvoudig beschikbaar op uw lokale bureaublad en kunnen deze worden gebruikt in alle native bureaubladtoepassingen. Elementen kunnen worden voorvertoond, geopend in systeemeigen desktoptoepassingen, onthuld in Mac Finder of Windows Verkenner voor plaatsing in andere documenten en lokaal worden gewijzigd. De wijzigingen worden weer opgeslagen in [!DNL Experience Manager] wanneer u de bestanden uploadt en er een nieuwe versie wordt gemaakt in de opslagplaats.

Een dergelijke integratie maakt verschillende rollen in de organisatie mogelijk om

* Beheer de elementen centraal in [!DNL Experience Manager Assets].

* Open de middelen in om het even welke inheemse Desktoptoepassingen, met inbegrip van derdetoepassingen en in Adobe Creative Cloud. De gebruikers kunnen zich daarbij gemakkelijk aan de verschillende normen houden, waaronder branding.

Als u [!DNL Experience Manager]-bureaubladtoepassing wilt gebruiken,

* Zorg ervoor dat uw [!DNL Experience Manager]-versie wordt ondersteund door de [!DNL Experience Manager]-bureaubladtoepassing. Zie de [systeemvereisten](release-notes.md).

* Download en installeer de toepassing. Zie [Desktop app](#install-v2) hieronder installeren.

* Test de verbinding met behulp van een paar elementen. Zie [hoe u naar elementen kunt bladeren en deze kunt zoeken](using.md#browse-search-preview-assets).

## Systeemvereisten, vereisten en downloadkoppelingen {#tech-specs-v2}

Zie de [[!DNL Experience Manager] Opmerkingen bij de release van de bureaubladtoepassing](release-notes.md) voor gedetailleerde informatie.

## Upgrade uitvoeren vanaf een vorige versie {#upgrade-from-previous-version}

Als u een gebruiker bent van v1.x van de bureaubladtoepassing, begrijpt u de verschillen en overeenkomsten tussen de vorige en de laatste versie van de app. Zie [nieuw in desktop app](introduction.md#whats-new-v2) en [hoe de app werkt](release-notes.md#how-app-works)

>[!NOTE]
>
>Twee versies van de bureaubladtoepassing kunnen niet naast elkaar bestaan op een computer. Verwijder de andere versie voordat u een versie installeert.

Voer de volgende instructies uit om een upgrade uit te voeren van een vorige versie van de app:

1. Voordat u de upgrade uitvoert, synchroniseert u al uw middelen en uploadt u uw wijzigingen naar [!DNL Experience Manager]. Zo voorkomt u dat bewerkingen verloren gaan wanneer u de app verwijdert.

1. Verwijder de vorige versie van de app. Selecteer bij het verwijderen de optie om de cache te wissen.

1. Start de computer opnieuw op.

1. [Download en ](release-notes.md)   [](#install-v2) installeer de nieuwste app. Volg de onderstaande instructies.

## {#install-v2} installeren

Voer de volgende stappen uit om de bureaubladtoepassing te installeren. Verwijder bestaande Adobe [!DNL Experience Manager] desktop app v1.x voordat u de nieuwste app installeert. Zie hierboven voor meer informatie.

1. Download het meest recente installatieprogramma van de [releaseopmerkingen](release-notes.md) pagina.

1. Houd de URL en de referenties van uw [!DNL Experience Manager]-implementatie handig.

1. Zie [Desktop app upgraden](#upgrade-from-previous-version) als u een upgrade uitvoert vanaf een andere versie van de app.

1. Sla deze stap over als u [!DNL Experience Manager] als [!DNL Cloud Service], [!DNL Experience Manager] 6.4.4 of later, of [!DNL Experience Manager] 6.5.0 of later gebruikt. Zorg ervoor dat uw [!DNL Experience Manager] opstelling aan de verenigbaarheidsvereisten voldoet die in [versienota&#39;s](release-notes.md) worden vermeld. Download indien nodig het toepasselijke [compatibiliteitspakket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) en installeer dit met [!DNL Experience Manager] Package Manager als een [!DNL Experience Manager]-beheerder. Als u een pakket wilt installeren, raadpleegt u [Werken met pakketten](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html).

1. Voer binair het installatieprogramma uit en volg de instructies op het scherm om te installeren.

1. In Windows wordt mogelijk `Visual Studio C++ Redistributable 2015` gevraagd te installeren. Volg de aanwijzingen op het scherm om de installatie uit te voeren. Als de installatie mislukt, wordt deze handmatig geïnstalleerd. Download het installatieprogramma van [hier](https://www.microsoft.com/en-us/download/details.aspx?id=52685) en installeer zowel `vc_redist.x64.exe`- als `vc_redist.x86.exe`-bestanden. Voer het installatieprogramma voor de [!DNL Experience Manager]-bureaubladtoepassing opnieuw uit.

1. Start de computer opnieuw naar wens. Start en configureer de bureaubladtoepassing.

1. Als u de app wilt verbinden met een [!DNL Experience Manager]-opslagplaats, klikt u op het pictogram van de app in de lade en start u de app. Geef het adres van de [!DNL Experience Manager]-server op in de notatie `https://[aem_server]:[port]/`.

   Klik op **[!UICONTROL Connect]** en geef de referenties op.

   ![Verbindingsscherm van bureaubladtoepassing met invoerserveradres](assets/connect_da2.png)

   *Afbeelding: Verbindingsscherm met invoerserveradres.*

   >[!CAUTION]
   >
   >Zorg ervoor dat er geen voorloopspaties of navolgende spaties zijn voor of na het adres van de [!DNL Experience Manager]-server. Anders kan de toepassing geen verbinding maken met de [!DNL Experience Manager]-server.

1. Als de verbinding is gelukt, kunt u de lijst met mappen en middelen weergeven die beschikbaar zijn in de hoofdmap van de [!DNL Experience Manager] DAM. U kunt vanuit de app door de mappen bladeren.

   ![Bij aanmelding wordt de DAM-inhoud weergegeven in de toepassing](assets/firstview_da2.png)

   *Afbeelding: De toepassing geeft de DAM-inhoud weer na de aanmelding*

1. ([!DNL Experience Manager] 6.5.1 of hoger) Als u bureaubladtoepassing gebruikt met [!DNL Experience Manager] 6.5.1 of hoger, upgrade S3 of Azure-aansluiting naar versie 1.10.4 of hoger. Zie [Azure-connector](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#azure-data-store) of [S3-connector](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#amazon-s-data-store).

   Neem contact op met de klantenservice van Adobe als u een klant van Adobe Managed Services (AMS) bent.

## Voorkeuren instellen {#set-preferences}

Als u de voorkeuren wilt wijzigen, klikt u op ![Meer optiepictogram](assets/do-not-localize/more_options_da2.png) en **[!UICONTROL Preference]** ![Voorkeurspictogram](assets/do-not-localize/preferences_icon_da2.png). Pas in het venster **[!UICONTROL Preferences]** de waarden van het volgende aan:

* [!UICONTROL Launch application on login].

* [!UICONTROL Show window when application starts].

* **[!UICONTROL Cache Directory]**: Locatie van de lokale cache van de app (deze bevat de lokaal gedownloade elementen).

* **[!UICONTROL Network Drive Letter]**: De stationsletter die wordt gebruikt om toe te wijzen aan  [!DNL Experience Manager] DAM. Wijzig dit niet als u het niet zeker weet. De app kan aan elke stationsletter in Windows worden toegewezen. Als twee gebruikers elementen van verschillende stationsletters plaatsen, kunnen ze de elementen die door elkaar zijn geplaatst niet zien. Het pad van de elementen wordt gewijzigd. De elementen blijven in het binaire bestand (bijvoorbeeld INDD) staan en worden niet verwijderd. In de app worden alle beschikbare stationsletters vermeld en wordt standaard de laatst beschikbare letter gebruikt die doorgaans `Z` is.

* **[!UICONTROL Maximum Cache Size]**: Toegestane cache op de vaste schijf in GB die wordt gebruikt voor het opslaan van lokaal gedownloade elementen.

* **[!UICONTROL Current cache size]**: Opslaggrootte van de lokaal gedownloade elementen. De informatie wordt alleen weergegeven nadat middelen zijn gedownload met de app.

* **[!UICONTROL Automatically download linked assets]**: De elementen die in de ondersteunde native Creative Cloud-apps worden geplaatst, worden automatisch opgehaald wanneer u het oorspronkelijke bestand downloadt.

* **[!UICONTROL Maximum number of downloads]**:  ![waarschuwingspictogramWijzigen met ](assets/do-not-localize/caution-icon.png) voorzichtigheid. Wanneer voor het eerst elementen worden gedownload (via de optie Tonen, Openen, Bewerken, Downloaden of een vergelijkbare optie), worden de elementen alleen gedownload als de batch minder dan dit nummer bevat. De standaardwaarde is 50. Niet wijzigen als u het niet zeker weet. Als u de waarde verhoogt, kan het langer duren en als u de waarde verlaagt, kunt u de benodigde elementen of mappen mogelijk niet in één keer downloaden.

* **[!UICONTROL Use legacy conventions when creating nodes for assets and folders]**:  ![waarschuwingspictogramWijzigen met ](assets/do-not-localize/caution-icon.png) voorzichtigheid. Met deze instelling kan de toepassing het gedrag van de v1.10-app emuleren tijdens het uploaden van mappen. In v1.10, respecteren de knoopnamen die in de bewaarplaats worden gecreeerd ruimten en het omhulsel van de omslagnamen die door de gebruiker worden verstrekt. In versie 2.1 van de app worden de extra spaties in de mapnamen echter geconverteerd naar streepjes. Als u bijvoorbeeld `New Folder` of `new   folder` uploadt, wordt hetzelfde knooppunt in de repository gemaakt als de optie niet is geselecteerd en het standaardgedrag in v2.1 behouden blijft. Als deze optie is geselecteerd, worden in de opslagplaats voor de bovenstaande twee mappen verschillende knooppunten gemaakt die overeenkomen met de werking van de v1.10-app.

   Het standaardgedrag van v2.1 blijft gelijk, dat wil zeggen, vervangt meerdere spaties in mapnamen door streepjes in de naam van de opslagplaats en zet deze om in namen van kleine letters.

* **[!UICONTROL Upload Acceleration]**:  ![waarschuwingspictogramWijzigen met ](assets/do-not-localize/caution-icon.png) voorzichtigheid. Bij het uploaden van elementen kan de toepassing gelijktijdige uploads gebruiken om de uploadsnelheid te verbeteren. U kunt de gelijktijdige uitvoering van het uploaden verhogen door de schuifregelaar naar rechts te verplaatsen. De schuifregelaar aan de linkerkant betekent geen gelijktijdige uitvoering (single-threaded upload), de middelste positie komt overeen met 10 gelijktijdige threads en de maximale limiet aan de rechterkant komt overeen met 20 gelijktijdige threads. Een hogere gelijktijdige limiet is meer hulpbronnenintensief.

Als u de niet-beschikbare voorkeuren wilt bijwerken, meldt u zich af bij de [!DNL Experience Manager]-server en werkt u de voorkeuren vervolgens bij. Nadat u de voorkeuren hebt bijgewerkt, klikt u op ![Voorkeuren opslaan](assets/do-not-localize/save_preferences_da2.png).

![Voorkeuren en instellingen voor de bureaubladtoepassing](assets/preferences_da2.png)

*Afbeelding: App-voorkeuren voor bureaublad.*

### Proxyondersteuning {#proxy-support}

[!DNL Experience Manager] desktop-app gebruikt de vooraf gedefinieerde proxy van het systeem om via HTTPS verbinding te maken met internet. De toepassing kan alleen verbinding maken met een netwerkproxy waarvoor geen extra verificatie is vereist.

Als u de instellingen van de proxyserver voor Windows configureert of wijzigt (Internetopties > LAN-instellingen), start u de [!DNL Experience Manager]-bureaubladtoepassing opnieuw om de wijzigingen van kracht te laten worden. Proxyconfiguratie wordt toegepast wanneer u de bureaubladtoepassing start. Sluit de app en start de app opnieuw om de wijzigingen door te voeren.

Als voor uw proxy verificatie is vereist, kan het IT-team de [!DNL Experience Manager Assets]-URL in de instellingen van de proxyserver toestaan dat het toepassingsverkeer wordt doorgegeven.

## De toepassing {#uninstall-the-app} verwijderen

Voer de volgende stappen uit om de installatie van de toepassing in Windows ongedaan te maken:

1. Upload al uw wijzigingen naar [!DNL Experience Manager] om te voorkomen dat u bewerkingen kwijtraakt. Zie [Elementen bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets). Log uit en [!UICONTROL Exit] de app.

1. Verwijder de app als u andere besturingssysteemtoepassingen verwijdert. Verwijder de software uit de programma&#39;s Toevoegen en Verwijderen in Windows.

1. Als u de cache en logbestanden wilt verwijderen, schakelt u het vereiste selectievakje in.

   ![Dialoogvenster verwijderen om logbestanden en cache te verwijderen](assets/uninstall_da2.png)

1. Volg de aanwijzingen op het scherm. Start de computer opnieuw op als deze klaar is.

Voer de volgende stappen uit om de installatie van de toepassing op de Mac te verwijderen:

1. Upload al uw wijzigingen naar [!DNL Experience Manager] om te voorkomen dat u bewerkingen kwijtraakt. Zie [Elementen bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets). Log uit en [!UICONTROL Exit] de app.

1. Verwijder `Adobe Experience Manager Desktop.app` uit `/Applications`.

Als u de interne cache van toepassingen op de Mac wilt opschonen en de toepassing wilt verwijderen, kunt u de volgende opdracht ook in de terminal uitvoeren:

```shell
/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh
```
