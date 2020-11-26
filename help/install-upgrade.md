---
title: Adobe Experience Manager-bureaubladtoepassing installeren en configureren
description: Installeer en configureer de Adobe Experience Manager-bureaubladtoepassing zodat deze kan werken met Adobe Experience Manager Assets-servers en download de middelen naar uw lokale bestandssysteem.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.5/ASSETS, SG_EXPERIENCEMANAGER/6.4/ASSETS, SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2893fc1f8aad02e1436a1a281a320e6837487220
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---


# Adobe Experience Manager-bureaubladtoepassing installeren {#install-app-v2}

Met de Adobe Experience Manager-bureaubladtoepassing zijn de middelen in de Experience Manager eenvoudig beschikbaar op uw lokale bureaublad en kunnen deze worden gebruikt in alle native bureaubladtoepassingen. Elementen kunnen worden voorvertoond, geopend in systeemeigen desktoptoepassingen, onthuld in Mac Finder of Windows Verkenner voor plaatsing in andere documenten en lokaal worden gewijzigd. De wijzigingen worden teruggezet naar de Experience Manager wanneer u de bestanden uploadt en er wordt een nieuwe versie gemaakt in de opslagplaats.

Een dergelijke integratie maakt verschillende rollen in de organisatie mogelijk om

* Beheer de elementen centraal in Experience Manager Assets.

* Open de middelen in om het even welke inheemse Desktoptoepassingen, met inbegrip van derdetoepassingen en in Adobe Creative Cloud. De gebruikers kunnen zich daarbij gemakkelijk aan de verschillende normen houden, waaronder branding.

Om Experience Manager desktop app te gebruiken,

* Zorg ervoor dat uw versie van de Experience Manager door de Desktop app van de Experience Manager wordt gesteund. Zie de [systeemvereisten](release-notes.md#system-requirements-and-prerequisites-v2) hieronder.

* Download en installeer de toepassing. Zie Desktop-app [hieronder](#install-v2) installeren.

* Test de verbinding met behulp van een paar elementen. Zie [hoe u naar elementen](using.md#browse-search-preview-assets)kunt bladeren en deze kunt zoeken.

## Systeemvereisten, vereisten en downloadkoppelingen {#tech-specs-v2}

Zie de opmerkingen bij de release van de [Experience Manager desktop app voor meer informatie](release-notes.md).

## Upgrade uitvoeren vanaf een vorige versie {#upgrade-from-previous-version}

Als u een gebruiker bent van v1.x van de bureaubladtoepassing, begrijpt u de verschillen en overeenkomsten tussen de vorige en de laatste versie van de app. Bekijk [wat er nieuw is in de bureaubladtoepassing](introduction.md#whats-new-v2) en [hoe de app werkt](release-notes.md#how-app-works)

>[!NOTE]
>
>Twee versies van de bureaubladtoepassing kunnen niet naast elkaar bestaan op een computer. Verwijder de andere versie voordat u een versie installeert.

Voer de volgende instructies uit om een upgrade uit te voeren van een vorige versie van de app:

1. Voordat u de upgrade uitvoert, synchroniseert u al uw middelen en uploadt u uw wijzigingen naar de Experience Manager. Zo voorkomt u dat bewerkingen verloren gaan wanneer u de app verwijdert.

1. Verwijder de vorige versie van de app. Selecteer bij het verwijderen de optie om de cache te wissen.

1. Start de computer opnieuw op.

1. [Download](release-notes.md) en [installeer](#install-v2) de nieuwste app. Volg de onderstaande instructies.

## Installeren {#install-v2}

Voer de volgende stappen uit om de bureaubladtoepassing te installeren. Verwijder bestaande Adobe Experience Manager-bureaubladtoepassing v1.x voordat u de nieuwste app installeert. Zie hierboven voor meer informatie.

1. Download het meest recente installatieprogramma van de pagina met [opmerkingen](release-notes.md) bij de release.

1. Houd URL en geloofsbrieven van uw plaatsing van de Experience Manager handig.

1. Zie Desktop-app [](#upgrade-from-previous-version)upgraden als u een upgrade uitvoert vanaf een andere versie van de app.

1. Sla deze stap over als u Experience Manager als Cloud Service, Experience Manager 6.4.4 of later, of Experience Manager 6.5.0 of later gebruikt. Zorg ervoor dat uw Experience Manager voldoet aan de compatibiliteitsvereisten die in de [releaseopmerkingen](release-notes.md)worden vermeld. Download indien nodig het toepasselijke [compatibiliteitspakket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) en installeer dit met de Experience Manager Package Manager als beheerder van de Experience Manager. Om een pakket te installeren, zie [hoe te met Pakketten](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html)werken.

1. Voer binair het installatieprogramma uit en volg de instructies op het scherm om te installeren.

1. In Windows wordt mogelijk gevraagd het installatieprogramma te installeren `Visual Studio C++ Redistributable 2015`. Volg de aanwijzingen op het scherm om de installatie uit te voeren. Als de installatie mislukt, wordt deze handmatig geïnstalleerd. Download het installatieprogramma van [hier](https://www.microsoft.com/en-us/download/details.aspx?id=52685) en installeer zowel `vc_redist.x64.exe` als `vc_redist.x86.exe` bestanden. Voer het installatieprogramma van de [!DNL Experience Manager] bureaubladtoepassing opnieuw uit.

1. Start de computer opnieuw naar wens. Start en configureer de bureaubladtoepassing.

1. Als u de app wilt verbinden met een [!DNL Experience Manager] repository, klikt u op het app-pictogram in de lade en start u de app. Geef het adres van de [!DNL Experience Manager] server op in de notatie `https://[aem_server]:[port]/`.

   Klik op de referenties **[!UICONTROL Connect]** en geef deze op.

   ![Verbindingsscherm van bureaubladtoepassing met invoerserveradres](assets/connect_da2.png)

   *Afbeelding: Verbindingsscherm met invoerserveradres.*

   >[!CAUTION]
   >
   >Zorg ervoor dat er geen voorloopspaties of navolgende spaties zijn voor of na het adres van de [!DNL Experience Manager] server. Anders kan de toepassing geen verbinding maken met de [!DNL Experience Manager] server.

1. Als de verbinding is gelukt, kunt u de lijst met mappen en middelen weergeven die beschikbaar zijn in de hoofdmap van de [!DNL Experience Manager] DAM. U kunt vanuit de app door de mappen bladeren.

   ![Bij aanmelding wordt de DAM-inhoud weergegeven in de toepassing](assets/firstview_da2.png)

   *Afbeelding: De toepassing geeft de DAM-inhoud weer na de aanmelding*

1. (Experience Manager 6.5.1 of hoger) Als u bureaubladtoepassingen gebruikt met Experience Manager 6.5.1 of hoger, moet u de S3- of Azure-aansluiting upgraden naar versie 1.10.4 of hoger. Zie [Azure-connector](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#azure-data-store) of [S3-connector](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/data-store-config.html#amazon-s-data-store).

   Neem contact op met de klantenservice van Adobe als u een klant van Adobe Managed Services (AMS) bent.

## Voorkeuren instellen {#set-preferences}

Als u de voorkeuren wilt wijzigen, klikt u op het pictogram ![](assets/do-not-localize/more_options_da2.png) Meer opties en het pictogram **[!UICONTROL Preference]** Voorkeuren ![](assets/do-not-localize/preferences_icon_da2.png). Pas in het **[!UICONTROL Preferences]** venster de waarden van het volgende aan:

* [!UICONTROL Launch application on login].

* [!UICONTROL Show window when application starts].

* **[!UICONTROL Cache Directory]**: Locatie van de lokale cache van de app (deze bevat de lokaal gedownloade elementen).

* **[!UICONTROL Network Drive Letter]**: De stationsletter die wordt gebruikt om toe te wijzen aan [!DNL Experience Manager] DAM. Wijzig dit niet als u het niet zeker weet. De app kan aan elke stationsletter in Windows worden toegewezen. Als twee gebruikers elementen van verschillende stationsletters plaatsen, kunnen ze de elementen die door elkaar zijn geplaatst niet zien. Het pad van de elementen wordt gewijzigd. De elementen blijven in het binaire bestand (bijvoorbeeld INDD) staan en worden niet verwijderd. In de app worden alle beschikbare stationsletters vermeld en wordt standaard de laatst beschikbare letter gebruikt die normaal gesproken `Z`is.

* **[!UICONTROL Maximum Cache Size]**: Toegestane cache op de vaste schijf in GB die wordt gebruikt voor het opslaan van lokaal gedownloade elementen.

* **[!UICONTROL Current cache size]**: Opslaggrootte van de lokaal gedownloade elementen. De informatie wordt alleen weergegeven nadat middelen zijn gedownload met de app.

* **[!UICONTROL Automatically download linked assets]**: De elementen die in de ondersteunde native Creative Cloud-apps worden geplaatst, worden automatisch opgehaald wanneer u het oorspronkelijke bestand downloadt.

* **[!UICONTROL Maximum number of downloads]**: Wanneer voor het eerst elementen worden gedownload (via de optie Tonen, Openen, Bewerken, Downloaden of een vergelijkbare optie), worden de elementen alleen gedownload als de batch minder dan dit nummer bevat. De standaardwaarde is 50. Niet wijzigen als u het niet zeker weet. Als u de waarde verhoogt, kan het langer duren en als u de waarde verlaagt, kunt u de benodigde elementen of mappen mogelijk niet in één keer downloaden.

* **[!UICONTROL Upload Acceleration]**: Bij het uploaden van elementen kan de toepassing gelijktijdige uploads gebruiken om de uploadsnelheid te verbeteren. U kunt de gelijktijdige uitvoering van het uploaden verhogen door de schuifregelaar naar rechts te verplaatsen. De schuifregelaar aan de linkerkant betekent geen gelijktijdige uitvoering (single-threaded upload), de middelste positie komt overeen met 10 gelijktijdige threads en de maximale limiet aan de rechterkant komt overeen met 20 gelijktijdige threads. Voor een hogere limiet voor gelijktijdige aanschaf is een hoger verbruik van bronnen van de processor van de lokale computer vereist.

Meld u af bij de [!DNL Experience Manager] server om de niet-beschikbare voorkeuren bij te werken. Nadat u de voorkeuren hebt bijgewerkt, klikt u op Voorkeuren ![](assets/do-not-localize/save_preferences_da2.png) opslaan om de wijzigingen op te slaan.

![Voorkeuren en instellingen voor de bureaubladtoepassing](assets/preferences_da2.png)

*Afbeelding: App-voorkeuren voor bureaublad.*

## De toepassing verwijderen {#uninstall-the-app}

Voer de volgende stappen uit om de installatie van de toepassing in Windows ongedaan te maken:

1. Upload al uw wijzigingen om te voorkomen dat u bewerkingen verliest. [!DNL Experience Manager] Zie Elementen [bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets). Log uit en [!UICONTROL Exit] de app.

1. Verwijder de app als u andere besturingssysteemtoepassingen verwijdert. Verwijder de software uit de programma&#39;s Toevoegen en Verwijderen in Windows.

1. Als u de cache en logbestanden wilt verwijderen, schakelt u het vereiste selectievakje in.

   ![Dialoogvenster verwijderen om logbestanden en cache te verwijderen](assets/uninstall_da2.png)

1. Volg de aanwijzingen op het scherm. Start de computer opnieuw op als deze klaar is.

Voer de volgende stappen uit om de installatie van de toepassing op de Mac te verwijderen:

1. Upload al uw wijzigingen om te voorkomen dat u bewerkingen verliest. [!DNL Experience Manager] Zie Elementen [bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets). Log uit en [!UICONTROL Exit] de app.

1. Verwijder het `Adobe Experience Manager Desktop.app` uit `/Applications`.

Als u de interne cache van toepassingen op de Mac wilt opschonen en de toepassing wilt verwijderen, kunt u de volgende opdracht ook in de terminal uitvoeren:

```shell
/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh
```
