---
title: AEM-bureaubladtoepassing versie 1.x gebruiken
description: Leer hoe u Adobe Experience Manager desktop app versie 1.x gebruikt en uw werk optimaliseert met middelen op het bureaublad.
uuid: 55057617-89de-43cd-8419-1252a42ab2fb
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 39d7bcad-d7b0-4978-a790-4cb68b8a7d6a
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b92e47456f9e16c24eac43d1c5fef9a582f143b5

---


# AEM-bureaubladtoepassing v1.x gebruiken {#use-aem-desktop-app-v1x}

Met de app zijn de elementen in AEM gemakkelijk toegankelijk op uw lokale bureaublad en kunnen deze worden gebruikt in alle bureaubladtoepassingen. Middelen kunnen eenvoudig worden weergegeven in de Finder van Mac of in Windows Verkenner, worden geopend in bureaubladtoepassingen en lokaal worden gewijzigd. De wijzigingen worden weer opgeslagen in AEM met een nieuwe versie die in de opslagplaats is gemaakt.

Dankzij een dergelijke integratie kunnen verschillende functies in de organisatie de middelen centraal beheren in AEM Assets en deze openen in Creative Cloud en andere toepassingen, terwijl het eenvoudig wordt om aan de verschillende standaarden, waaronder branding, te voldoen.

De belangrijkste taken die u uitvoert met de AEM-bureaubladtoepassing v1 zijn:

* [Verbinding maken met een AEM-server](#installandconnect)

* [Elementen rechtstreeks openen op bureaublad](#openondesktop)
* [Elementen van het bureaublad bewerken en uitchecken](#workonassets)

* [Elementen en mappen bulksgewijs uploaden](#bulkupload)

Raadpleeg de [aanbevolen procedures voor het gebruik van apps](best-practices-for-v1.md)voor de verschillende aanbevolen en niet-aanbevolen taken. Als u problemen ondervindt met de toepassing, kunt u zien hoe u [problemen met AEM Desktop](troubleshoot-app-v1.md)kunt oplossen.

>[!NOTE]
>De AEM-bureaubladtoepassing werd geïntroduceerd in de release van AEM 6.1 en heet AEM Assets Companion App.

## Aanraakpunten met de AEM Desktop-app in de creatieve workflow {#aem-desktop-app-touch-points-in-the-creative-workflow}

De app AEM Desktop integreert, samen met AEM Assets, in uw creatieve workflow en biedt de volgende aanraakpunten.

![De AEM Desktop-app tikt de creatieve workflow aan](assets/aem_desktopapp_workflow.png)

De AEM Desktop-app tikt de creatieve workflow aan

## AEM-bureaubladtoepassing installeren en verbinden met AEM-server {#installandconnect}

Voordat u kunt beginnen met het maken of bewerken van creatieve middelen, sluit u de bureaubladtoepassing aan op de AEM Assets-server om elementen te downloaden en uploaden naar de opslagplaats. Voer de volgende taken uit:

1. [Installeer de app](#installapp).
1. [Stel uw voorkeuren](#inapppref) en verbindingsgegevens in.
1. [Maak verbinding met een AEM-server](#connect) en koppel elementen als opslagplaats voor lokale stations.
1. [Schakel bureaubladacties](#desktopactions) op de AEM-server in.

De AEM-bureaubladtoepassing gebruikt een HTTPS-verbinding om verbinding te maken met de AEM-server om uw middelen op krachtige en veilige wijze over te brengen.

>[!NOTE]
>Voor een deel van of alle installatie en configuratiestappen, kunt u hulp van uw beheerder AEM of systeembeheerder nodig hebben.

### De toepassing installeren {#installapp}

Als u de AEM-bureaubladtoepassing wilt gebruiken, moet u ervoor zorgen dat uw AEM-serverversie wordt ondersteund door de AEM Desktop-app. Download het juiste (binaire) installatiebestand voor uw besturingssysteem (Mac of Windows) en installeer de toepassing.

Afhankelijk van uw netwerk- en systeemvoorkeuren kan een gedetailleerde configuratie nodig zijn. Zie [De AEM Desktop-app](install-configure-app-v1.md) installeren en configureren voor meer informatie.

1. Ga naar de downloadpagina [voor de](https://helpx.adobe.com/experience-manager/kb/download-companion-app.html) AEM Desktop-app en download de juiste binaire code voor uw besturingssysteem.
1. Start het gedownloade installatiebestand en volg de aanwijzingen op het scherm om de app te installeren.

   >[!NOTE]
   >Er kan slechts één exemplaar van de AEM-bureaubladtoepassing worden geïnstalleerd en tegelijkertijd actief zijn.

### Begrijp de opties en voorkeuren in de app {#inapppref}

De toepassing stelt instellingen in staat om verbinding te maken met en de verbinding met AEM-servers te verbreken, de status van geüploade bestanden weer te geven, de lokale cache te beheren, enzovoort. De standaardinstellingen werken voor een standaardgebruiker van de toepassing. U kunt de instellingen aanpassen om meer uit de toepassing te halen en de integratie met de AEM-server te beëindigen. De verschillende instellingen worden hieronder in detail beschreven.

**Verken middelen** De lokale schijf openen waarop de AEM Assets-opslagplaats is gemonteerd. Met andere woorden, verken de middelen die nu op uw lokale computer beschikbaar worden gesteld.

**Elementstatus** weergeven Wanneer gewijzigde elementen worden geüpload of nieuwe elementen worden toegevoegd aan de AEM Assets-opslagplaats, worden de elementen op de achtergrond geüpload. Met de uploaden naar de achtergrond kunt u vloeiende bewerkingen uitvoeren, zonder dat u hoeft te wachten tot het uploaden is voltooid, met name voor grote elementen. U kunt uw wijzigingen lokaal opslaan en deze vergeten. Het duurt enige tijd voordat de toepassing deze middelen naar de server verzendt, afhankelijk van de beschikbare bandbreedte. U kunt de status van de upload controleren, samen met wat meer basisinformatie.

**Opties** voor klikken/tikken op Opties in de toepassingsmap van AEM Desktop om instellingen te openen waarmee de toepassing wordt gestart wanneer uw systeem wordt gestart. verbinding maken met de AEM-server wanneer de app wordt gestart; en om de lokale stationsletter te veranderen waar de Middelen van AEM na het opzetten beschikbaar zijn.

**Geavanceerd > Cache** beheren U kunt bepalen hoeveel schijfruimte beschikbaar is voor lokale cachedoeleinden. De artefacten van de server van Activa AEM worden in het voorgeheugen ondergebracht voor een vlottere ervaring. U kunt de standaardinstellingen aanpassen aan uw wensen. Bovendien kunt u de cache wissen om alle elementen opnieuw op te halen. Als u de cache wist, blijven de niet-opgeslagen wijzigingen behouden. Elementen die niet zijn aangemeld bij de AEM-server, blijven behouden en worden niet verwijderd.

### Verbinding maken met een AEM-server {#connect}

De toepassing ondersteunt proxyconfiguratie op Mac en Windows. De configuratie wordt gelezen wanneer de app wordt gestart. Als u proxyinstellingen wijzigt, start u de toepassing opnieuw zodat de wijzigingen van kracht worden.

>[!NOTE]
>
>Als u de proxyinstellingen wijzigt, start u de toepassing opnieuw zodat de wijzigingen van kracht worden. Anders blijft de toepassing de eerder geconfigureerde proxyserver gebruiken.

1. Start de AEM Desktop-app. Als u uw AEM-instantie aan de app wilt toewijzen, geeft u de AEM-server op in de indeling `https://[aem-server-url]:[port]`.

   ![Verifiëren op Mac en URL van AEM-server opgeven](assets/aem_desktop_app_server_url.png)

1. Geef in het aanmeldingsscherm de gebruikersnaam en het wachtwoord voor de instantie op. Als u een alternatieve AEM-instantie wilt opgeven, selecteert u de **[!UICONTROL Alternate Login URL]** optie.

   ![Geef AEM-serverreferenties op in het aanmeldingsscherm op AEM Desktop](assets/chlimage_1-2.png)

### Desktopacties inschakelen in AEM-webinterface {#desktopactions}

Vanuit de interface Middelen in een browser kunt u de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw desktoptoepassing. Deze opties worden Desktophandelingen genoemd en worden niet standaard ingeschakeld. Voer de volgende stappen uit om deze in te schakelen.

1. Klik of tik in de middelenconsole op het pictogram **Gebruiker** op de werkbalk.
1. Klik of tik op het pictogram **[!UICONTROL My Preferences]** om het **[!UICONTROL Preferences]** dialoogvenster weer te geven.
1. Selecteer in het dialoogvenster Gebruikersvoorkeuren **[!UICONTROL Show Desktop Actions For Assets]**. Klik of tik op **[!UICONTROL Accept]**.

   ![Schakel Bureaubladhandelingen weergeven voor elementen in om bureaubladhandelingen in te schakelen](assets/chlimage_1-3.png)

   Schakel Bureaubladhandelingen weergeven voor elementen in om bureaubladhandelingen in te schakelen

## Elementen openen en openen op uw bureaublad {#openondesktop}

>[!NOTE]
>In Windows voorkomt u met de [standaardinstelling](https://support.microsoft.com/en-us/kb/2668751) voor Windows 7 dat AEM-bureaubladtoepassingen elementen verwerken die groter zijn dan 50 MB.

### De locatie van toegewezen elementen vanuit de AEM-webinterface onthullen {#reveal-the-location-of-mapped-assets-from-aem-web-interface}

Nadat u de AEM Assets-opslagplaats aan uw lokale schijf hebt toegewezen, kunt u extra pictogrammen inschakelen en de functie Map uploaden weergeven voor de toegewezen elementen en mappen.

1. Open de AEM Assets-interface en houd de aanwijzer boven een map of element om de bureaubladacties als snelle acties weer te geven in de kaartweergave.

   ![Open in de gebruikersinterface Elementen het menu Snel handelen om acties op het bureaublad weer te geven](assets/chlimage_1-4.png)

   Open in de gebruikersinterface Elementen het menu Snel handelen om acties op het bureaublad weer te geven

   Deze acties zijn ook beschikbaar als u op het pictogram **Bureaubladhandelingen** op de werkbalk klikt of tikt nadat u het element of de werkbalk op de elementpagina hebt geselecteerd.

1. Als u het element wilt openen in de bureaubladtoepassing die is gekoppeld aan de specifieke bestandsextensie, klikt of tikt u op de actie **Openen op bureaublad** , snel op het pictogram ![](assets/aemassets_icon_openondesktop.png)Openen op bureaublad.

   U kunt ook **Openen** kiezen in het menu **Bureaubladhandelingen** op de werkbalk.

1. Klik of tik op het pictogram **Snelle actie** onthullen ![](assets/aemassets_reveal_icon.png) om het specifieke element op uw lokale bestandssysteem te zoeken.

   U kunt ook **Tonen** kiezen in het menu **Bureaubladhandelingen** op de werkbalk.

### AEM-elementen openen vanuit de Finder of de Explorer {#open-aem-assets-from-the-finder-or-the-explorer}

Selecteer op de Mac de optie Openen in het contextmenu om een element te openen via AEM Desktop.

Selecteer voor Adobe InDesign-bestanden (INDD-bestanden) **[!UICONTROL Open]** in het contextmenu. Wanneer u op deze optie klikt, downloadt de app de gekoppelde middelen naar uw lokale bestandssysteem en wordt het INDD-bestand in Adobe InDesign geopend. Deze methode zorgt ervoor dat de benodigde elementen lokaal beschikbaar zijn wanneer u het INDD-bestand bewerkt.

In Windows selecteert u Openen op web in het contextmenu om het element te openen. Klik/tik op het pictogram ![](assets/aemassets_icon_openondesktop.png) Openen op bureaublad in het venster Asset Status (Asset Status) om het element te openen.

![Contextmenu-opties voor toegang tot en het openen van middelen met de AEM Desktop-app](assets/aem_desktopapp_mac_context_menu.png)

Contextmenu-opties voor toegang tot en het openen van middelen met de AEM Desktop-app

### De status van elementen begrijpen {#understand-the-asset-statuses}

| ![Standaardpictogram Windows-app](assets/win_default.png) | De toepassing is verbonden met de server en alle elementen zijn gesynchroniseerd. |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Pictogram Windows uitgeschakeld](assets/win_disabled.png) | De toepassing wordt gestart, maar heeft geen verbinding met de server. Sommige elementen zijn mogelijk in afwachting van synchronisatie. |
| ![Windows-pictogram voor bestandssync](assets/win_sync.png) | Elementen worden gesynchroniseerd. Bestanden worden geüpload of gedownload. U kunt de exacte status zien en de overdrachten pauzeren vanuit het venster Asset Status. |
| ![Windows-pictogram Opnieuw verbinden](assets/win_refresh.png) | App probeert opnieuw verbinding te maken. Mogelijk zorgen de netwerkproblemen ervoor dat de verbinding wordt verbroken. |

## Werken met uw elementen {#workonassets}

### Elementen uitchecken via de AEM-webinterface {#check-out-assets-from-the-aem-web-interface}

Met AEM-middelen kunt u elementen uitchecken en ze weer inchecken nadat u de wijzigingen hebt aangebracht. Nadat u een element hebt uitgecheckt, kunt u het element alleen bewerken, annoteren, publiceren, verplaatsen of verwijderen. Als u een element uitcheckt, vergrendelt u het element en voorkomt u dat andere gebruikers deze bewerkingen uitvoeren. Om activa te kunnen uitchecken/inchecken, hebt u schrijftoegang op hen nodig.

Er zijn twee manieren om elementen uit de AEM-webinterface te controleren. Voor gedetailleerde informatie over de eerste methode raadpleegt u de [inchecken en uitchecken van bestanden in de interface](https://docs.adobe.com/content/help/en/experience-manager-65/assets/managing/check-out-and-submit-assets.html)Middelen. Voer de volgende stappen uit voor de tweede methoden om het element uit te checken en te openen wanneer de AEM Desktop-app is geïnstalleerd.

1. Open de AEM Assets-interface en houd de aanwijzer boven een map of element om de bureaubladacties als snelle acties weer te geven in de kaartweergave.

   ![Eigenschappen, optie in Kaartweergave](assets/chlimage_1-4.png)

   Deze bureaubladacties zijn ook beschikbaar wanneer u op het pictogram Bureaubladhandelingen op de werkbalk klikt of tikt nadat u het element of de werkbalk op de elementpagina hebt geselecteerd.

1. Als u het element wilt openen, klikt of tikt u op het pictogram ![](assets/aemassets_icon_openondesktop.png)Openen op bureaublad.

   U kunt ook Openen kiezen in het menu Bureaubladhandelingen op de werkbalk.

   >[!NOTE]
   >Wanneer u een bestand bewerkt dat net is geopend en niet is uitgecheckt, weten andere gebruikers niet dat een element door u wordt bijgewerkt.

1. Als u middelen wilt openen om te bewerken in een Adobe Creative Cloud-toepassing, klikt of tikt u op het pictogram Bureaublad bewerken in de modus Snel ![bewerken](assets/aemassets_icon_editdesktop.png). Hierdoor wordt het element ook uitgecheckt voor bewerking. Nadat u klaar bent met bewerken, checkt u het element in om de wijzigingen in AEM-elementen bij te werken.

   U kunt ook Bewerken kiezen in het menu Bureaubladhandelingen op de werkbalk.

1. Selecteer de menuoptie Openen. De geselecteerde elementen worden geopend in de voorvertoningsmodus.
1. Selecteer de optie Bewerken om de elementen te bewerken. De elementen worden geopend in de bewerkingsmodus.

### Elementen uitchecken op de Mac {#check-out-assets-on-mac}

Met de app kunt u elementbestanden uitchecken om te voorkomen dat andere gebruikers de bestanden waaraan u werkt, kunnen wijzigen.

1. Selecteer in het contextmenu van Mac de AEM Assets-map openen om Finder te openen.

   ![Contextmenu-opties voor toegang tot en het openen van middelen met de AEM Desktop-app](assets/aem_desktopapp_mac_context_menu.png)

   Contextmenu-opties voor toegang tot en het openen van middelen met de AEM Desktop-app

1. Navigeer naar het element dat u wilt uitchecken.

   ![Openen in contextmenu van AEM Assets op Mac](assets/chlimage_1-5.png)

1. Klik met de rechtermuisknop op het element en selecteer Meer informatie over elementen in het contextmenu.
1. Klik/tik op het pictogram Uitchecken in het dialoogvenster Asset Info om het element uit te checken. Het pictogram Uitchecken schakelt over naar het pictogram voor inchecken nadat u erop hebt geklikt of getikt.

   ![Bladeren naar middel om af te rekenen](assets/chlimage_1-6.png)

1. Als u het element wilt inchecken zodat het beschikbaar is voor andere gebruikers, klikt of tikt u op het incheckpictogram in het dialoogvenster Elementinfo.

### Elementen in Windows uitchecken {#check-out-assets-on-windows}

Met de app kunt u elementbestanden uitchecken om te voorkomen dat andere gebruikers de bestanden waaraan u werkt, kunnen wijzigen.

1. Selecteer in het contextmenu de optie Middelen verkennen om Verkenner te openen.
1. Navigeer in Verkenner naar de locatie van het element dat u wilt uitchecken.

   ![Schakelen tussen selectievakjes](assets/chlimage_1-7.png)

1. Klik met de rechtermuisknop op het element en selecteer Openen op web in het contextmenu.
1. Klik/tik op het pictogram Uitchecken in het dialoogvenster Asset Info. Met het pictogram Uitchecken schakelt u over naar het incheckpictogram.

   ![Schakelen tussen selectievakjes](assets/chlimage_1-8.png)

1. Controleer het element in Verkenner. Het vergrendelingspictogram op het ![middelenvergrendelingspictogram](assets/aemassets_icon_lockcheckout.png) geeft aan dat u het element hebt uitgecheckt.

   >[!NOTE]
   >Het slotpictogram kan na een paar minuten vertraging verschijnen. De AEM Desktop-app slaat de middelen in de cache op zodat het even kan duren voordat de vergrendelde status wordt bijgewerkt.

1. Als u het element wilt inchecken zodat het beschikbaar is voor andere gebruikers, klikt of tikt u op het incheckpictogram in het dialoogvenster **Elementinfo** .

### Middelen inchecken met Finder of Explorer en webinterface gebruiken {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface}

Wanneer u klaar bent met het bewerken van de elementen, slaat u de elementen op in uw bureaubladtoepassing. Selecteer Meer informatie over elementen in het contextmenu en klik of tik op Inchecken.

De elementen worden geüpload naar de AEM-server. U kunt desgewenst de status van de upload controleren door Asset Status weergeven te selecteren in het taakbalkpictogram.

![Statusvenster voor bestandsoverdracht en uploaden van AEM Desktop](assets/aem_desktopapp_upload_status.png)

U kunt een element ook inchecken via de AEM-webinterface. Klik of tik op de uitgecheckte elementen of selecteer deze. Klik/tik op het pictogram voor het ![inchecken van het pictogram](assets/aemassets_icon_checkin.png)op de werkbalk.

### Elementen en mappen uploaden in bulk naar AEM-server {#bulkupload}

Met AEM Desktop kunt u een volledige map met elementen uit uw lokale bestandsmap uploaden naar AEM Assets. Op deze manier worden alle elementen in de map in bulk geüpload in plaats van ze een voor een te hoeven uploaden.

1. Klik in de interface Middelen op **Maken** of tik op de werkbalk en kies Map **** uploaden in het menu.
1. Blader naar de map die u wilt uploaden en selecteer deze.
1. Klik op OK/tik op OK. In het dialoogvenster Elementstatus wordt de status van de upload weergegeven.

   ![Zie de status van de upload in het venster Asset Status](assets/aem_desktopapp_bulkupload_status.png)

   Zie de status van de upload in het venster Asset Status

   >[!NOTE]
   >U kunt het uploaden handmatig pauzeren of annuleren door op het juiste pictogram te klikken of erop te tikken.

1. Nadat de map is geüpload, sluit u het dialoogvenster en gaat u naar de interface Middelen. De geüploade map wordt weergegeven in de webinterface.

Houd er rekening mee dat het *niet wordt aanbevolen* om een groter aantal bestanden/geneste mappen van uw lokale schijf in Finder of Explorer te kopiëren en te plakken of te slepen naar het gedeelde netwerkgebied dat wordt toegewezen door de AEM-bureaubladtoepassing. Deze map is veel minder betrouwbaar dan de hierboven beschreven functie Map uploaden.

Als u liever op het bureaublad werkt, selecteert u bestanden/mappen die u naar AEM wilt uploaden in Finder of Explorer, kopieert u deze naar het systeemklembord, navigeert u naar de doelmap in het gebied voor delen van het netwerk en selecteert u in het contextmenu van de AEM-bureaubladtoepassing de optie Middelen plakken. Op deze manier begint de AEM-bureaubladtoepassing met het uploaden van de geplakte middelen, vergelijkbaar met de hierboven beschreven Upload-map.

>[!MORELIKETHIS]
>
>* [Inleiding tot AEM-bureaubladtoepassing](https://helpx.adobe.com/customer-care-office-hours/aem/desktop-app.html)
>* [Inchecken/uitchecken begrijpen met AEM-bureaubladtoepassing](https://docs.adobe.com/content/help/en/experience-manager-learn/assets/collaboration/checkin-checkout-technical-video-understand.html)
>* [Problemen met AEM Desktop-toepassing oplossen](troubleshoot-app-v1.md)

