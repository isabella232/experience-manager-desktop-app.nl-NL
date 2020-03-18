---
title: Adobe Experience Manager-bureaubladtoepassing installeren en configureren
description: Installeer en configureer de Adobe Experience Manager-bureaubladtoepassing voor gebruik met Adobe Experience Manager-middelenservers en download de middelen op uw lokale bestandssysteem.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ac4be2cb69a112f393ec76d5d95987634d0c9c46

---


# Adobe Experience Manager-bureaubladtoepassing installeren {#install-app-v2}

Met de Adobe Experience Manager-bureaubladtoepassing zijn de middelen in Experience Manager gemakkelijk toegankelijk op uw lokale bureaublad en kunnen deze worden gebruikt in alle bureaubladtoepassingen. Elementen kunnen eenvoudig worden weergegeven in de Finder van Mac of in Windows Verkenner, worden geopend in bureaubladtoepassingen en lokaal worden gewijzigd. De wijzigingen worden weer opgeslagen in Experience Manager wanneer u de bestanden uploadt en er een nieuwe versie wordt gemaakt in de opslagplaats.

Dankzij een dergelijke integratie kunnen verschillende functies in de organisatie de middelen centraal beheren in Adobe Experience Manager Assets en deze openen in Creative Cloud en andere toepassingen, terwijl u zich eenvoudig aan de verschillende standaarden kunt houden, waaronder branding.

U kunt als volgt de Experience Manager-bureaubladtoepassing gebruiken:

* Zorg ervoor dat de versie van uw Experience Manager-server wordt ondersteund door de Desktop-app Experience Manager. Zie de [compatibiliteitsmatrix](release-notes-of-v1.md#compatibilitymatrix).
* Download en installeer de toepassing.
* Test de verbinding met behulp van een paar elementen. Zie [Toegang tot middelen en open elementen op uw bureaublad](use-app-v1.md#openondesktop).

## Voorwaarden voor systeemvereisten en downloadkoppelingen {#tech-specs-v2}

Raadpleeg de opmerkingen bij de release [Experience Manager voor meer informatie](release-notes.md).

## Upgrade van app v1.x naar app v2 {#upgrade-from-previous-version}

Als u een bestaande gebruiker van de app bent, begrijpt u de verschillen en overeenkomsten tussen de vorige en de laatste versie van de app. Volg ook de onderstaande richtlijnen om van v1.x naar de nieuwste versie over te schakelen.

>[!NOTE]
>
>Desktop-app v1.x en v2 kunnen niet samen op een computer bestaan. Verwijder de andere versie voordat u een versie installeert.

Als u een upgrade wilt uitvoeren van v1.x naar de nieuwste versie van de app, volgt u de volgende instructies:

1. Synchroniseer al uw middelen voordat u de upgrade uitvoert. Upload alle wijzigingen met app v1.x. Hiermee voorkomt u dat wijzigingen verloren gaan wanneer u app v1.x verwijdert.
1. Verwijder app v1.x. Wis de cache wanneer u v1.x verwijdert.
1. Start de computer opnieuw op.
1. Download en installeer de nieuwste app. Volg de onderstaande instructies.

## Installeren {#install-v2}

Voer de volgende stappen uit om de bureaubladtoepassing te installeren. Verwijder bestaande Adobe Experience Manager-bureaubladtoepassing v1.x voordat u de nieuwste app installeert. Zie hierboven voor meer informatie.

1. Houd de URL en de referenties van uw AEM-implementatie handig.
1. Sla deze stap over als u AEM 6.4.4 en hoger of AEM 6.5.0 of hoger gebruikt. Zorg ervoor dat uw AEM-installatie voldoet aan de compatibiliteitsvereisten die in de opmerkingen bij de release worden vermeld. Download indien nodig het toepasselijke [compatibiliteitspakket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq640/featurepack/adobe-asset-link-support) en installeer dit met de AEM Package Manager als AEM-beheerder. Om een pakket te installeren, zie [hoe te met Pakketten](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html)werken.
1. Voer binair het installatieprogramma uit en volg de instructies op het scherm om te installeren.
1. In Windows wordt mogelijk gevraagd het installatieprogramma te installeren `Visual Studio C++ Redistributable 2015`. Volg de aanwijzingen op het scherm om de installatie uit te voeren. Als de installatie mislukt, wordt deze handmatig geïnstalleerd. Download het installatieprogramma van [hier](https://www.microsoft.com/en-us/download/details.aspx?id=52685) en installeer zowel `vc_redist.x64.exe` als `vc_redist.x86.exe` bestanden. Voer het installatieprogramma van de AEM-bureaubladtoepassing opnieuw uit.
1. Start de computer opnieuw naar wens. Start de bureaubladtoepassing om deze te configureren.
1. Als u de app wilt verbinden met een AEM-opslagplaats, klikt u op het pictogram van de app in de lade om de app te starten. Geef het adres van de AEM-instantie op. Klik op de referenties **[!UICONTROL Connect]** en geef deze op.

   ![Verbindingsscherm van bureaubladtoepassing met invoerserver-](assets/connect_da2.png "adresVerbindingsscherm met invoerserveradres")

   >[!Cautie]
   >
   >Zorg ervoor dat er geen voorloopspaties of navolgende spaties zijn vóór of na het adres van de AEM-server. Anders kan de toepassing geen verbinding maken met de AEM-server.

1. Als de verbinding is gelukt, kunt u de lijst met mappen en middelen weergeven die beschikbaar zijn in de hoofdmap van AEM DAM. U kunt vanuit de app door de mappen bladeren.

   ![Bij het aanmelden geeft de app de DAM-](assets/firstview_da2.png "inhoud weer. Bij het aanmelden geeft de app de DAM-inhoud weer")

1. (AEM 6.5.1 of hoger) Als u bureaubladtoepassingen gebruikt met AEM 6.5.1 of hoger, moet u de S3- of Azure-aansluiting upgraden naar versie 1.10.4 of hoger. Zie [Azure-connector](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html#AzureDataStore) of [S3-connector](https://helpx.adobe.com/experience-manager/6-5/sites/deploying/using/data-store-config.html#AmazonS3DataStore).

   Als u een klant van Adobe Managed Services (AMS) bent, neemt u contact op met de klantenservice van Adobe.

## Voorkeuren instellen {#set-preferences}

Als u de voorkeuren wilt wijzigen, klikt u op het pictogram ![](assets/do-not-localize/more_options_da2.png) Meer opties en het pictogram **[!UICONTROL Preference]** Voorkeuren ![](assets/do-not-localize/preferences_icon_da2.png). Pas in het **[!UICONTROL Preferences]** venster de waarden van het volgende aan:

* [!UICONTROL Launch application on login].
* [!UICONTROL Show window when application starts].
* **[!UICONTROL Cache Directory]**: Locatie van de lokale cache van de app (deze bevat de lokaal gedownloade elementen).
* **[!UICONTROL Network Drive Letter]**: De stationsletter die wordt gebruikt om aan AEM DAM in kaart te brengen. Wijzig dit niet als u het niet zeker weet. De app kan aan elke stationsletter in Windows worden toegewezen. Als twee gebruikers elementen van verschillende stationsletters plaatsen, kunnen ze de elementen die door elkaar zijn geplaatst niet zien. Het pad van de elementen wordt gewijzigd. De elementen blijven in het binaire bestand (bijvoorbeeld INDD) staan en worden niet verwijderd. In de app worden alle beschikbare stationsletters vermeld en wordt standaard de laatst beschikbare letter gebruikt die normaal gesproken `Z`is.
* **[!UICONTROL Maximum Cache Size]**: Toegestane cache op de vaste schijf in GB die wordt gebruikt voor het opslaan van lokaal gedownloade elementen.
* **[!UICONTROL Current cache size]**: Opslaggrootte van de lokaal gedownloade elementen. De informatie wordt alleen weergegeven nadat middelen zijn gedownload met de app.
* **[!UICONTROL Automatically download linked assets]**: De middelen die in de ondersteunde native Creative Cloud-toepassingen worden geplaatst, worden automatisch opgehaald wanneer u het oorspronkelijke bestand downloadt.
* **[!UICONTROL Maximum number of downloads]**: Wanneer voor het eerst elementen worden gedownload (via de optie Tonen, Openen, Bewerken, Downloaden of een vergelijkbare optie), worden de elementen alleen gedownload als de batch minder dan dit nummer bevat. De standaardwaarde is 50. Niet wijzigen als u het niet zeker weet. Als u de waarde verhoogt, kan het langer duren en als u de waarde verlaagt, kunt u de benodigde elementen of mappen mogelijk niet in één keer downloaden.

Meld u af bij de AEM-server om de niet-beschikbare voorkeuren bij te werken. Nadat u de voorkeuren hebt bijgewerkt, klikt u op Voorkeuren ![](assets/do-not-localize/save_preferences_da2.png) opslaan om de wijzigingen op te slaan.

![Voorkeuren en](assets/preferences_da2.png "instellingen voor de app AEM-bureaubladApp-voorkeuren voor bureaublad")

## De toepassing verwijderen {#uninstall-the-app}

Voer de volgende stappen uit om de installatie van de toepassing in Windows ongedaan te maken:

1. Upload al uw wijzigingen naar AEM om te voorkomen dat er bewerkingen verloren gaan. Zie Elementen [bewerken en bijgewerkte elementen uploaden naar AEM](using.md#edit-assets-upload-updated-assets). Log uit en [!UICONTROL Exit] de app.
1. Verwijder de app als u andere besturingssysteemtoepassingen verwijdert. Verwijder de software uit de programma&#39;s Toevoegen en Verwijderen in Windows.
1. Als u de cache en logbestanden wilt verwijderen, schakelt u het vereiste selectievakje in.
   ![Dialoogvenster voor het verwijderen van logbestanden en](assets/uninstall_da2.png "cachegeheugenHet dialoogvenster voor het verwijderen van logbestanden en cache")
1. Volg de aanwijzingen op het scherm. Start de computer opnieuw op als deze klaar is.

Voer de volgende stappen uit om de installatie van de toepassing op de Mac te verwijderen:

1. Upload al uw wijzigingen naar AEM om te voorkomen dat er bewerkingen verloren gaan. Zie Elementen [bewerken en bijgewerkte elementen uploaden naar AEM](using.md#edit-assets-upload-updated-assets). Log uit en [!UICONTROL Exit] de app.
1. Verwijder het `Adobe Experience Manager Desktop.app` uit `/Applications`.

Als u de interne cache van toepassingen op de Mac wilt opschonen en de toepassing wilt verwijderen, kunt u de volgende opdracht ook in de terminal uitvoeren:
`/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh`
