---
title: Gebruik AEM bureaubladtoepassing versie 1.x.
description: Leer hoe u Adobe Experience Manager desktop app versie 1.x gebruikt en uw werk optimaliseert met middelen op het bureaublad.
contentOwner: AG
translation-type: tm+mt
source-git-commit: 200135fb96bbfcf9f72e857514bb9b71a88ed817
workflow-type: tm+mt
source-wordcount: '2472'
ht-degree: 0%

---


# AEM desktop app v1.x gebruiken {#use-aem-desktop-app-v1x}

Met de app zijn de middelen in AEM gemakkelijk toegankelijk op uw lokale bureaublad en kunnen deze in alle bureaubladtoepassingen worden gebruikt. Middelen kunnen eenvoudig worden weergegeven in de Finder van Mac of in Windows Verkenner, worden geopend in bureaubladtoepassingen en lokaal worden gewijzigd. De wijzigingen worden weer opgeslagen in AEM met een nieuwe versie die in de opslagplaats is gemaakt.

Een dergelijke integratie maakt het mogelijk dat verschillende rollen in de organisatie de bedrijfsmiddelen centraal in AEM Assets beheren en ze in de Creative Cloud en andere toepassingen benaderen, terwijl het eenvoudig wordt om de verschillende normen, waaronder branding, na te leven.

De belangrijkste taken die u uitvoert met de AEM desktop app v1 zijn:

1. [Verbinding maken met een AEM server](#installandconnect)
1. [Elementen rechtstreeks openen op bureaublad](#openondesktop)
1. [Elementen van het bureaublad bewerken en uitchecken](#workonassets)
1. [Elementen en mappen bulksgewijs uploaden](#bulkupload)

Raadpleeg de [aanbevolen procedures voor het gebruik van apps](best-practices-for-v1.md)voor de verschillende aanbevolen en niet-aanbevolen taken. Als u problemen ondervindt met de app, kunt u zien hoe u problemen [kunt oplossen AEM bureaublad](troubleshoot-app-v1.md).

>[!NOTE]
>
>AEM desktop app werd geïntroduceerd in AEM 6.1 release en heet AEM Assets Companion App.

## Aanraakpunten AEM desktop-app in de creatieve workflow {#aem-desktop-app-touch-points-in-the-creative-workflow}

AEM Desktop-app integreert, samen met AEM Assets, in uw creatieve workflow en biedt de volgende aanraakpunten.

![AEM Desktop app touch wijst de creatieve workflow aan](assets/aem_desktopapp_workflow.png)

AEM Desktop app touch wijst de creatieve workflow aan

## Installeer en verbind AEM bureaubladtoepassing met AEM server {#installandconnect}

Voordat u kunt beginnen met het maken of bewerken van creatieve middelen, sluit u de bureaubladtoepassing aan op de AEM Assets-server om elementen te downloaden en uploaden naar de opslagplaats. Voer de volgende taken uit:

1. [Installeer de app](#installapp).
1. [Stel uw voorkeuren](#inapppref) en verbindingsgegevens in.
1. [Maak verbinding met een AEM server](#connect) en koppel elementen in de opslagplaats als lokaal station.
1. [Schakel bureaubladhandelingen](#desktopactions) op AEM server in.

AEM desktop-app gebruikt een HTTPS-verbinding om verbinding te maken met AEM server om uw middelen op robuuste en veilige wijze over te brengen.

>[!NOTE]
>
>Voor een deel van of alle installatie en configuratiestappen, kunt u hulp van uw AEM beheerder of systeembeheerder nodig hebben.

### De toepassing installeren {#installapp}

Als u AEM bureaubladtoepassing wilt gebruiken, moet u ervoor zorgen dat uw AEM serverversie wordt ondersteund door AEM bureaubladtoepassing. Download het juiste (binaire) installatiebestand voor uw besturingssysteem (Mac of Windows) en installeer de toepassing.

Afhankelijk van uw netwerk- en systeemvoorkeuren kan een gedetailleerde configuratie nodig zijn. Zie [Installeer en vorm AEM Desktop app](install-configure-app-v1.md) voor meer informatie.

1. Ga naar de downloadpagina [van de](https://helpx.adobe.com/experience-manager/kb/download-companion-app.html) AEM Desktop-app en download de juiste binaire code voor uw besturingssysteem.
1. Start het gedownloade installatiebestand en volg de aanwijzingen op het scherm om de app te installeren.

   >[!NOTE]
   >
   >Er kan slechts één exemplaar van de AEM-bureaubladtoepassing worden geïnstalleerd en tegelijkertijd actief zijn.

### Begrijp de opties en voorkeuren in de app {#inapppref}

De toepassing stelt instellingen in staat verbinding te maken met en de verbinding met AEM servers te verbreken, de status van geüploade bestanden weer te geven, de lokale cache te beheren, enzovoort. De standaardinstellingen werken voor een standaardgebruiker van de toepassing. U kunt de instellingen aanpassen om meer uit de toepassing te halen en de integratie met AEM server te beëindigen. De verschillende instellingen worden hieronder in detail beschreven.

**Verken middelen** De lokale schijf openen waarop de AEM Assets-opslagplaats is gemonteerd. Met andere woorden, verken de middelen die nu op uw lokale computer beschikbaar worden gesteld.

**Elementstatus** weergeven Wanneer gewijzigde elementen worden geüpload of nieuwe elementen worden toegevoegd aan de AEM Assets-opslagplaats, worden de elementen op de achtergrond geüpload. Met de uploaden naar de achtergrond kunt u vloeiende bewerkingen uitvoeren, zonder dat u hoeft te wachten tot het uploaden is voltooid, met name voor grote elementen. U kunt uw wijzigingen lokaal opslaan en deze vergeten. Het duurt enige tijd voordat de toepassing deze middelen naar de server verzendt, afhankelijk van de beschikbare bandbreedte. U kunt de status van de upload controleren, samen met wat meer basisinformatie.

**Opties** voor klikken/tikken op Opties in de AEM-bureaubladtoepassingslade voor toegang tot instellingen om de toepassing te starten wanneer uw systeem wordt gestart. verbinding maken met de AEM server wanneer de app wordt gestart; en om de lokale stationsletter te veranderen waar AEM Assets na het opzetten beschikbaar is.

**Geavanceerd > Cache** beheren U kunt bepalen hoeveel schijfruimte beschikbaar is voor lokale cachedoeleinden. De artefacten van de AEM Assets-server worden lokaal in het cachegeheugen opgeslagen voor een vloeiender ervaring. U kunt de standaardinstellingen aanpassen aan uw wensen. Bovendien kunt u de cache wissen om alle elementen opnieuw op te halen. Als u de cache wist, blijven de niet-opgeslagen wijzigingen behouden. Elementen die niet in AEM server zijn ingecheckt, blijven behouden en worden niet verwijderd.

### Verbinding maken met een AEM server {#connect}

De toepassing ondersteunt proxyconfiguratie op Mac en Windows. De configuratie wordt gelezen wanneer de app wordt gestart. Als u proxyinstellingen wijzigt, start u de toepassing opnieuw zodat de wijzigingen van kracht worden.

>[!NOTE]
>
>Als u de proxyinstellingen wijzigt, start u de toepassing opnieuw zodat de wijzigingen van kracht worden. Anders blijft de toepassing de eerder geconfigureerde proxyserver gebruiken.

1. Start AEM Desktop-app. Als u uw AEM met de app wilt toewijzen, geeft u de AEM-server op in de indeling `https://[aem-server-url]:[port]`.

   ![Verifiëren op Mac en URL van AEM server opgeven](assets/aem_desktop_app_server_url.png)

1. Geef in het aanmeldingsscherm de gebruikersnaam en het wachtwoord voor de instantie op. Selecteer de **[!UICONTROL Alternate Login URL]** optie als u een alternatieve AEM wilt opgeven.

   ![Geef AEM serverreferenties op in het aanmeldingsscherm van AEM bureaubladtoepassing](assets/login_screen_v1.png)

### Desktopacties inschakelen in AEM webinterface {#desktopactions}

Vanuit de gebruikersinterface Middelen kunt u de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw desktoptoepassing. Deze opties worden desktophandelingen genoemd en worden niet standaard ingeschakeld. Voer de volgende stappen uit om deze in te schakelen.

1. Klik/tik op het gebruikerspictogram in de rechterbovenhoek van de werkbalk van de interface Middelen.
1. Klik **[!UICONTROL My Preferences]** om het **[!UICONTROL Preferences]** dialoogvenster weer te geven.

   ![AEM interface met gebruikersvoorkeuren](assets/aem_ui_user_preferences.png)

1. Selecteer in het dialoogvenster Gebruikersvoorkeuren **[!UICONTROL Show Desktop Actions For Assets]**. Klik op **[!UICONTROL Accept]**.

   ![Inschakelen [!UICONTROL Show Desktop Actions For Assets] van desktophandelingen](assets/enable_desktop_actions.png)

   *Afbeelding: Schakel Bureaubladhandelingen weergeven voor elementen in om de bureaubladacties in te schakelen.*

## Elementen openen en openen op uw bureaublad {#openondesktop}

Wanneer u op **Openen** klikt om een element op de lokale computer te openen, wordt het element naar de interne cache gedownload. De app start de native bureaubladtoepassing die is gekoppeld aan het bestandstype van het gedownloade element.

Selecteer in Mac de optie **Openen** in het contextmenu om een element te openen via AEM bureaubladtoepassing. In Windows selecteert u Openen op web in het contextmenu om het element te openen. Klik/tik op het pictogram ![](assets/do-not-localize/aemassets_icon_openondesktop.png) Openen op bureaublad in het venster Asset Status (Asset Status) om het element te openen.

Selecteer voor Adobe InDesign-bestanden (INDD) een optie in het **[!UICONTROL Open]** contextmenu. Wanneer u op deze optie klikt, downloadt de app de gekoppelde elementen naar uw lokale bestandssysteem en wordt het INDD-bestand in Adobe InDesign geopend. Deze methode zorgt ervoor dat de benodigde elementen lokaal beschikbaar zijn wanneer u het INDD-bestand bewerkt.

![Contextmenu-opties voor toegang tot en het openen van middelen met AEM Desktop-app](assets/aem_desktopapp_mac_context_menu.png)

*Afbeelding: Opties in contextmenu voor het openen en openen van middelen met AEM bureaubladtoepassing.*

>[!NOTE]
>
>In Windows voorkomt de [standaard Windows 7-instelling](https://support.microsoft.com/en-us/kb/2668751) dat AEM bureaubladtoepassing elementen verwerkt die groter zijn dan 50 MB.

>[!NOTE]
>
>Adobe raadt u aan naar de Finder View Options op de Mac te gaan en de opties **Show item info**, **Show item preview** en **Show preview column** voor de gekoppelde AEM Assets folder uit te schakelen. Het verbetert de prestaties.

### Extra opties in AEM interface {#additional-options-in-aem-assets}

Nadat u de AEM Assets-opslagplaats aan uw lokale station hebt toegewezen, kunt u extra pictogrammen en de functie voor het uploaden van mappen inschakelen voor de toegewezen elementen en mappen.

1. Open de AEM Assets-interface en houd de aanwijzer boven een map of element om de desktophandelingen als snelle handelingen weer te geven in de kaartweergave.

   ![Open in de gebruikersinterface Elementen het menu Snel handelen om acties op het bureaublad weer te geven](assets/desktop_actions_in_card_view.png)

   *Afbeelding: Open in de interface Elementen het menu Handelingen Snel om acties op het bureaublad weer te geven.*

   Deze acties zijn ook beschikbaar als u op de werkbalk op de optie **Bureaubladhandelingen** klikt nadat u het element of de werkbalk op de elementpagina hebt geselecteerd.

1. Als u het element wilt openen in de bureaubladtoepassing die is gekoppeld aan de specifieke bestandsextensie, klikt u op de actie **Openen op bureaublad** , snel op het pictogram ![](assets/do-not-localize/aemassets_icon_openondesktop.png)Openen op bureaublad.

   U kunt ook **Openen** kiezen in het menu **Bureaubladhandelingen** op de werkbalk.

Als u het specifieke element op uw lokale bestandssysteem wilt zoeken, klikt u op **Snel optreden** onthullen ![](assets/do-not-localize/aemassets_reveal_icon.png). U kunt ook **Tonen** kiezen in het menu **Bureaubladhandelingen** op de werkbalk.

## De status van elementen begrijpen {#understand-the-asset-statuses}

| ![Standaardpictogram Windows-app](assets/do-not-localize/win_default.png) | De toepassing is verbonden met de server en alle elementen zijn gesynchroniseerd. |
--- |--- |
| ![Pictogram Windows uitgeschakeld](assets/do-not-localize/win_disabled.png) | De toepassing wordt gestart, maar heeft geen verbinding met de server. Sommige elementen zijn mogelijk in afwachting van synchronisatie. |
| ![Windows-pictogram voor bestandssync](assets/do-not-localize/win_sync.png) | Elementen worden gesynchroniseerd. Bestanden worden geüpload of gedownload. U kunt de exacte status zien en de overdrachten pauzeren vanuit het venster Asset Status. |
| ![Windows-pictogram Opnieuw verbinden](assets/do-not-localize/win_refresh.png) | App probeert opnieuw verbinding te maken. Mogelijk zorgen de netwerkproblemen ervoor dat de verbinding wordt verbroken. |

## Werken met uw elementen {#workonassets}

### Elementen uitchecken via de AEM webinterface {#check-out-assets-from-the-aem-web-interface}

Met AEM Assets kunt u elementen uitchecken om te bewerken en ze weer inchecken nadat u alle wijzigingen hebt aangebracht. Nadat u een element hebt uitgecheckt, kunt u het element alleen bewerken, annoteren, publiceren, verplaatsen of verwijderen. Als u een element uitcheckt, vergrendelt u het element en voorkomt u dat andere gebruikers deze bewerkingen uitvoeren. Om activa te kunnen uitchecken/inchecken, hebt u schrijftoegang op hen nodig.

Er zijn twee manieren om elementen uit de AEM webinterface te controleren. Voor gedetailleerde informatie over de eerste methode raadpleegt u de [inchecken en uitchecken van bestanden in de interface](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/check-out-and-submit-assets.html)Middelen. Voer de volgende stappen uit voor de tweede methoden om het element uit te checken en te openen wanneer AEM Desktop-app is geïnstalleerd.

1. Open de AEM Assets-interface en houd de aanwijzer boven een map of element om de desktophandelingen als snelle handelingen weer te geven in de kaartweergave.

   ![Eigenschappen, optie in Kaartweergave](assets/desktop_actions_in_card_view.png)

   Deze bureaubladacties zijn ook beschikbaar wanneer u op het pictogram Bureaubladhandelingen op de werkbalk klikt of tikt nadat u het element of de werkbalk op de elementpagina hebt geselecteerd.

1. Als u het element wilt openen, klikt of tikt u op het pictogram ![](assets/do-not-localize/aemassets_icon_openondesktop.png)Openen op bureaublad.

   U kunt ook Openen kiezen in het menu Bureaubladhandelingen op de werkbalk.

   >[!NOTE]
   >
   >Wanneer u een bestand bewerkt dat net is geopend en niet is uitgecheckt, weten andere gebruikers niet dat een element door u wordt bijgewerkt.

1. Als u middelen wilt openen om te bewerken in een Adobe Creative Cloud-toepassing, klikt of tikt u op het pictogram ![Bureaublad bewerken in de modus Snel](assets/do-not-localize/aemassets_icon_editdesktop.png)bewerken. Hierdoor wordt het element ook uitgecheckt voor bewerking. Nadat u klaar bent met bewerken, checkt u het element in om de wijzigingen in AEM Assets bij te werken.

   U kunt ook Bewerken kiezen in het menu Bureaubladhandelingen op de werkbalk.

1. Selecteer de menuoptie Openen. De geselecteerde elementen worden geopend in de voorvertoningsmodus.
1. Selecteer de optie Bewerken om de elementen te bewerken. De elementen worden geopend in de bewerkingsmodus.

### Elementen uitchecken vanuit Finder in Mac OS {#check-out-assets-on-mac}

Met de app kunt u elementbestanden uitchecken om te voorkomen dat andere gebruikers de bestanden waaraan u werkt, kunnen wijzigen.

1. Selecteer in het contextmenu van Mac de Open AEM Assets-map om Finder te openen.

   ![Contextmenu-opties voor toegang tot en het openen van middelen met AEM Desktop-app](assets/aem_desktopapp_mac_context_menu.png)

   Contextmenu-opties voor toegang tot en het openen van middelen met AEM Desktop-app

1. Navigeer naar het element dat u wilt uitchecken.
1. Klik met de rechtermuisknop op het element en selecteer Meer informatie over elementen in het contextmenu.
1. Klik/tik op het pictogram Uitchecken in het dialoogvenster Asset Info om het element uit te checken. Het pictogram Uitchecken schakelt over naar het pictogram voor inchecken nadat u erop hebt geklikt of getikt.

   ![Bladeren naar middel om af te rekenen](assets/browse_assets_to_checkout.png)

1. Als u het element wilt inchecken zodat het beschikbaar is voor andere gebruikers, klikt of tikt u op het incheckpictogram in het dialoogvenster Elementinfo.

### Elementen in Windows uitchecken {#check-out-assets-on-windows}

Met de app kunt u elementbestanden uitchecken om te voorkomen dat andere gebruikers de bestanden waaraan u werkt, kunnen wijzigen.

1. Selecteer in het contextmenu de optie Middelen verkennen om Verkenner te openen.
1. Navigeer in Verkenner naar de locatie van het element dat u wilt uitchecken.
1. Klik met de rechtermuisknop op het element en selecteer Openen op web in het contextmenu.
1. Klik/tik op het pictogram Uitchecken in het dialoogvenster Asset Info. Met het pictogram Uitchecken schakelt u over naar het incheckpictogram.

   ![Schakelen tussen selectievakjes](assets/checkout_icon_toggles.png)

1. Controleer het element in Verkenner. Het vergrendelingspictogram op het ![middelenvergrendelingspictogram](assets/do-not-localize/aemassets_icon_lockcheckout.png) geeft aan dat u het element hebt uitgecheckt.

   >[!NOTE]
   >
   >Het slotpictogram kan na wat vertraging verschijnen. AEM de bureaubladtoepassing plaatst de elementen in cache, zodat het even kan duren voordat de vergrendelde status wordt bijgewerkt.

1. Als u het element wilt inchecken zodat het beschikbaar is voor andere gebruikers, klikt of tikt u op het incheckpictogram in het dialoogvenster **Elementinfo** .

### Middelen inchecken met Finder of Explorer en webinterface gebruiken {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface}

Wanneer u klaar bent met het bewerken van de elementen, slaat u de elementen op in uw bureaubladtoepassing. Selecteer **Meer informatie over** elementen in het contextmenu en klik op Inchecken.

De elementen worden geüpload naar AEM server. U kunt desgewenst de status van de upload controleren door Asset Status **** weergeven te selecteren in het systeemvakpictogram. U kunt ook een middel inchecken via de AEM webinterface. Klik op de uitgecheckte elementen of selecteer deze. Klik in de werkbalk op het pictogram voor het ![inchecken van het pictogram](assets/do-not-localize/aemassets_icon_checkin.png).

Middelen worden automatisch naar AEM geüpload nadat eventuele wijzigingen lokaal zijn opgeslagen. Met het inchecken kunt u het element ter beschikking stellen van andere AEM gebruikers voor bewerking.

### Elementen en mappen uploaden naar AEM server opheffen {#bulkupload}

Met AEM Desktop kunt u een volledige map met elementen uit uw lokale bestandsmap uploaden naar AEM Assets. Op deze manier worden alle elementen in de map in bulk geüpload in plaats van ze een voor een te hoeven uploaden.

1. Klik in de interface Middelen op **Maken** of tik op de werkbalk en kies Map **** uploaden in het menu.
1. Blader naar de map die u wilt uploaden en selecteer deze.
1. Klik op OK/tik op OK. In het dialoogvenster Elementstatus wordt de status van de upload weergegeven.

   ![Zie de status van de upload in het venster Asset Status](assets/aem_desktopapp_bulkupload_status.png)

   Zie de status van de upload in het venster Asset Status

   >[!NOTE]
   >
   >U kunt het uploaden handmatig pauzeren of annuleren door op het juiste pictogram te klikken of erop te tikken.

1. Nadat de map is geüpload, sluit u het dialoogvenster en gaat u naar de interface Middelen. De geüploade map wordt weergegeven in de webinterface.

Adobe raadt u niet aan een groter aantal bestanden of geneste mappen vanuit het lokale bestandssysteem naar het gedeelde netwerkgebied te kopiëren en te plakken of te slepen. De toepassing kan het uploadproces niet beheren vanwege technische beperkingen en de prestaties zijn slecht.

U kunt ook bestanden/mappen selecteren waarnaar u wilt uploaden in AEM in Finder of Explorer, deze kopiëren naar het systeemklembord, naar de doelmap navigeren in het gebied voor delen van het netwerk en in het contextmenu van de AEM-bureaubladtoepassing de optie Middelen **** plakken selecteren. Op deze manier begint AEM bureaubladtoepassing de geplakte elementen te uploaden, vergelijkbaar met de optie Map **** uploaden die beschikbaar is in de AEM webinterface.

>[!MORELIKETHIS]
>
>* [Problemen met AEM bureaubladtoepassing oplossen](troubleshoot-app-v1.md)

