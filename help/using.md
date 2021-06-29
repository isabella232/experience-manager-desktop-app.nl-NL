---
title: Use [!DNL Experience Manager] desktop app
description: Gebruik [!DNL Adobe Experience Manager] desktop app, to work with [!DNL Adobe Experience Manager] DAM-middelen rechtstreeks van uw Win- of Mac-bureaublad en gebruik in andere toepassingen.
mini-toc-levels: 1
feature: Bureaubladtoepassing, beheer van bedrijfsmiddelen
exl-id: fa19d819-231a-4a01-bfd2-6bba6fec2f18
source-git-commit: dcd29d0bbb32004d970d334c256e659f4a4c39e1
workflow-type: tm+mt
source-wordcount: '4053'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager]-bureaubladtoepassing gebruiken {#use-aem-desktop-app-v2}

Gebruik de [!DNL Adobe Experience Manager]-bureaubladtoepassing om eenvoudig toegang te krijgen tot de digitale middelen in de DAM-opslagruimte [!DNL Adobe Experience Manager] op uw lokale bureaublad en deze middelen te gebruiken in alle bureaubladtoepassingen. U kunt de middelen in Desktoptoepassingen openen en de activa plaatselijk uitgeven - upload de veranderingen terug naar [!DNL Experience Manager] met versiecontrole, om de updates met andere gebruikers te delen. U kunt ook nieuwe bestanden en maphiërarchieën uploaden naar [!DNL Experience Manager], mappen maken en elementen of mappen verwijderen uit [!DNL Experience Manager] DAM.

Dankzij de integratie kunnen verschillende rollen in de organisatie de elementen centraal beheren in [!DNL Experience Manager Assets] en toegang krijgen tot de middelen op het lokale bureaublad in de native toepassingen op Windows of Mac OS.

Wanneer u de toepassing opent na het afmelden of voor het eerst, geef de URL van uw [!DNL Experience Manager]-server op in de notatie `https://[aem-server-url]:[port]/`. Selecteer vervolgens de optie [!UICONTROL Connect]. Geef referenties op om de toepassing te verbinden met de server.

De belangrijkste taken die u uitvoert met de [!DNL Experience Manager]-bureaubladtoepassing zijn:

![Workflows en taken die u kunt uitvoeren met  [!DNL Experience Manager] desktop ](assets/aem_desktop_app_usecases_v2.png "appWorkflows en taken die u kunt uitvoeren  [!DNL Adobe Experience Manager] met desktop ")
appDownload dit afdrukklare PDF-bestand  [](assets/aem_desktop_app_usecases_print.pdf) .

## Hoe desktop app werkt {#how-app-works2}

Voordat u de toepassing gaat gebruiken, moet u [weten hoe de toepassing werkt](release-notes.md#how-app-works). Zorg ook dat u bekend bent met de volgende termen:

* **[!UICONTROL Desktop Actions]**: Vanuit de webinterface Middelen kunt u vanuit een browser de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw native desktoptoepassing. Deze acties zijn beschikbaar via de webinterface en gebruiken de functionaliteit van de bureaubladtoepassing. Zie [hoe te om de Acties van de Desktop toe te laten](using.md#desktopactions-v2).

* Bestandsstatus is **[!UICONTROL Cloud Only]**: Dergelijke middelen worden niet op de lokale computer gedownload en zijn alleen beschikbaar op de [!DNL Experience Manager]-server.

* Bestandsstatus is **[!UICONTROL Available locally]**: De middelen worden gedownload en beschikbaar op de lokale computer zoals is. De elementen worden niet gewijzigd.

* Bestandsstatus is **[!UICONTROL Edited locally]**: Dergelijke elementen worden lokaal gewijzigd en de wijzigingen worden nog steeds naar de [!DNL Experience Manager]-server geüpload. Nadat u het uploadt, verandert de status in [!UICONTROL Available locally]. Zie [Elementen bewerken](using.md#edit-assets-upload-updated-assets).

* Bestandsstatus is **[!UICONTROL Editing conflict]**: Als u en andere gebruikers tegelijkertijd een element wijzigen, geeft de app aan dat er een bewerkingsconflict is opgetreden. De app biedt ook opties om uw wijzigingen te behouden of te negeren. Zie [hoe u bewerkingsconflicten kunt voorkomen](using.md#adv-workflow-collaborate-avoid-conflicts).

* Bestandsstatus is **[!UICONTROL Modified remotely]**: De app geeft aan of een element dat u hebt gedownload, is gewijzigd op de [!DNL Experience Manager]-server. De app biedt ook de optie om de nieuwste versie te downloaden en uw lokale kopie bij te werken. Zie [hoe u bewerkingsconflicten kunt voorkomen](using.md#adv-workflow-collaborate-avoid-conflicts).

* **[!UICONTROL Check-out]**: Als u een bestand bewerkt of van plan bent een bestand te bewerken, schakelt u de status in of uit. Er wordt een vergrendelingspictogram toegevoegd aan het element in de app en de webinterface [!DNL Experience Manager]. Met het vergrendelingspictogram kunnen andere gebruikers voorkomen dat hetzelfde element tegelijk wordt bewerkt, omdat dit tot een bewerkingsconflict leidt.

* **[!UICONTROL Check-in]**: Markeer het element als veilig voor andere gebruikers om het te bewerken zonder een bewerkingsconflict te veroorzaken. Wanneer u uw wijzigingen uploadt, wordt het vergrendelingspictogram automatisch verwijderd. Als u de incheck-status inschakelt, wordt ook het vergrendelingspictogram verwijderd. U wordt echter aangeraden dit niet handmatig in te checken zonder de wijzigingen te uploaden. Als u de wijzigingen verwijdert, schakelt u het inchecken handmatig in of uit.

* **[!UICONTROL Open]** handeling: Open gewoon het element om er een voorvertoning van weer te geven in de oorspronkelijke toepassing. Het wordt afgeraden het element met deze handeling te bewerken, omdat het element niet wordt uitgecheckt en andere gebruikers bewerkingen kunnen uitvoeren die tot bewerkingsconflicten leiden.

* **[!UICONTROL Edit]** handeling: Gebruik de handeling om de afbeelding te wijzigen. Als u op [!UICONTROL Edit] klikt, wordt het element automatisch uitgecheckt en wordt een vergrendelingspictogram toegevoegd aan het element. Klik op Bewerken als u het element niet wilt bewerken en klik vervolgens op [!UICONTROL Toggle check-in]. Als u elementen wilt verwijderen, hernoemen of verplaatsen in de DAM-maphiërarchie, gebruikt u de [!DNL Experience Manager]-webinterfacehandelingen en niet de bewerkingshandeling.[!DNL Experience Manager]

* **[!UICONTROL Download]** handeling: Download het middel naar uw lokale computer. U kunt de elementen nu downloaden en later bewerken. werk offline en upload de wijzigingen later. Elementen worden gedownload in een cachemap op uw bestandssysteem.

* **[!UICONTROL Reveal File]** of  **[!UICONTROL Reveal Folder]** actie: Terwijl de elementen naar een lokale cachemap worden gedownload, bootst de toepassing een lokale netwerkschijf na en biedt deze een lokaal pad voor elk element. Als u dit pad wilt weten, gebruikt u de desbetreffende openingsoptie in de app. U moet actie onthullen om elementen in de Creative Cloud-toepassing te plaatsen. Zie [Elementen plaatsen](using.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]** handeling: Als u het element wilt weergeven in de  [!DNL Experience Manager] webinterface, opent u het in de webinterface. U kunt meer werkstromen van [!DNL Experience Manager] interface zoals het bijwerken van meta-gegevens of activaontdekking in werking stellen.

* **[!UICONTROL Delete]** handeling: Verwijder het element uit de  [!DNL Experience Manager] DAM-opslagplaats. De actie schrapt de originele kopie van het middel op de server van de Experience Manager. Zie [Wijzigingen negeren](using.md#edit-assets-upload-updated-assets) als u alleen wijzigingen in het lokale element wilt negeren.

* **[!UICONTROL Upload Changes]**: De bureaubladtoepassing uploadt het bijgewerkte element alleen wanneer u het expliciet uploadt naar de  [!DNL Experience Manager] server. Wanneer u uw bewerkingen opslaat, worden de wijzigingen alleen op uw lokale computer opgeslagen. Tijdens het uploaden wordt het element automatisch ingecheckt en wordt het vergrendelingspictogram verwijderd. Zie [Elementen bewerken](using.md#edit-assets-upload-updated-assets).

## Desktopacties inschakelen in de webinterface [!DNL Experience Manager] {#desktopactions-v2}

Vanuit de [!DNL Assets]-gebruikersinterface in een browser kunt u de middelenlocaties verkennen of de middelen uitchecken en het middel openen voor bewerking in uw desktoptoepassing. Deze opties worden [!UICONTROL Desktop Actions] genoemd en niet door gebrek toegelaten. Voer de volgende stappen uit om deze functie in te schakelen.

1. Klik in de [!DNL Assets]-console op het pictogram **[!UICONTROL User]** op de werkbalk.
1. Klik op **[!UICONTROL My Preferences]** om het dialoogvenster **[!UICONTROL Preferences]** weer te geven.

1. Selecteer [!UICONTROL User Preferences] in het dialoogvenster **[!UICONTROL Show Desktop Actions For Assets]** en klik vervolgens op **[!UICONTROL Accept]**.


   ![Selecteer Bureaubladhandelingen weergeven voor elementen om bureaubladhandelingen in te schakelen](assets/enable_desktop_actions.png)

   *Afbeelding: Selecteer deze optie  [!UICONTROL Show Desktop Actions For Assets] om bureaubladhandelingen in te schakelen.*

## Zoeken, zoeken en voorvertonen van elementen {#browse-search-preview-assets}

U kunt vanuit de bureaubladtoepassing bladeren naar de middelen die beschikbaar zijn in de [!DNL Experience Manager]-opslagplaats, deze zoeken en er een voorvertoning van weergeven. Probeer het volgende in de app:

1. Blader naar een map en bekijk basisinformatie over de middelen die beschikbaar zijn in de map, samen met kleine miniaturen van alle elementen.

   ![Door de DAM-bestanden en -](assets/browse_folder_da2.png "mappen bladerenDoor de DAM-bestanden en -mappen bladeren")

1. Klik op de bestandsnaam als u meer informatie en een grotere miniatuur van een afzonderlijk element wilt bekijken.

   ![Een grotere voorvertoning van een element en ](assets/large_preview_actions_da2.png "handelingen bekijkenEen grotere voorvertoning van een element en handelingen bekijken")

1. Klik **[!UICONTROL Open]** of **[!UICONTROL Edit]** om het dossier plaatselijk te downloaden en enkel het te bekijken of het in de inheemse toepassing, respectievelijk uit te geven.
1. Zoek met behulp van trefwoorden naar een verwant element in de [!DNL Experience Manager]-opslagplaats. Gebruik `?` en `*` als vervangingen. Deze jokertekens vervangen een enkel teken of meerdere tekens. Filter de resultaten en sorteer deze zo nodig.

   ![Voorbeeld van zoeken met ](assets/search_wildcard_da2.png "jokerteken voor sterretjeVoorbeeld met jokerteken voor sterretje")

   ![Een andere voorbeeldzoekopdracht met ](assets/search_wildcard2_da2.png "jokerteken voor sterretjesEen andere voorbeeldzoekopdracht met andere plaatsing van jokerteken voor sterretjes")

>[!NOTE]
>
>In de app worden de elementen weergegeven door de zoekcriteria af te stemmen op meerdere metagegevensvelden en niet alleen op de titel van het element of de bestandsnaam.

## Elementen downloaden {#download-assets}

U kunt de elementen downloaden naar uw lokale bestandssysteem. De app haalt de middelen op van de [!DNL Experience Manager]-server en slaat dezelfde kopie op uw lokale bestandssysteem op.

Klik ![Meer optiepictogram](assets/do-not-localize/more2_da2.png) voor opties en klik ![Downloadpictogram](assets/do-not-localize/download_cloud_da2.png) om te downloaden.

![Downloadoptie voor een ](assets/download_option_da2.png "assetDownload-optie voor een element")

>[!NOTE]
>
>Wanneer u een groot bestand of een groot aantal bestanden downloadt of uploadt, schakelt de toepassing de handelingen voor elementen en mappen uit. De acties zijn beschikbaar wanneer het downloaden of uploaden is voltooid.

Het downloaden van meerdere elementen kan leiden tot slechte prestaties als de wachtrij groot is of als u te maken krijgt met een netwerkprobleem. Het is ook onbekend dat u veel bestanden in de wachtrij plaatst om te downloaden wanneer u een map downloadt. Om lange wachttijden te vermijden, beperkt app het aantal elementen dat in één keer wordt gedownload. Zie [Voorkeuren instellen](install-upgrade.md#set-preferences) voor informatie over het configureren van de voorkeuren. Zelfs onder deze limiet kan de app soms om bevestiging vragen voordat een ogenschijnlijk grote map wordt gedownload.

![App bevestigt download van relatief groot aantal ](assets/download_confirmation_da2.png "middelenApp bevestigt download van relatief groot aantal middelen")

Als er mappen zijn geselecteerd en gedownload, downloadt de toepassing alleen elementen die rechtstreeks in de map(pen) in [!DNL Experience Manager] zijn opgeslagen. Elementen worden niet automatisch uit submappen gedownload.

## Elementen op uw bureaublad openen {#openondesktop-v2}

U kunt de externe middelen openen voor weergave in de oorspronkelijke toepassing. De middelen worden gedownload aan een lokale omslag en gelanceerd in de inheemse toepassing verbonden aan het dossierformaat. U kunt de oorspronkelijke toepassing wijzigen en specifieke bestandstypen (extensies) openen in de Mac of Windows.

Klik **[!UICONTROL Open]** van het elementenmenu. Het element wordt lokaal gedownload en in de oorspronkelijke toepassing geopend. Controleer de voortgang van het downloaden en de overdrachtssnelheid van grote middelen op de statusbalk.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>Als de verwachte wijzigingen niet in de app worden weergegeven, klikt u op het pictogram Vernieuwen ![pictogram Vernieuwen](assets/do-not-localize/refresh.png) of klikt u met de rechtermuisknop in de app-interface en klikt u op **[!UICONTROL Refresh]**. De acties zijn niet beschikbaar wanneer grotere downloads of uploads worden uitgevoerd.

Als u de lokale downloadmap van een element wilt openen, klikt u op ![Meer handelingspictogram](assets/do-not-localize/more2_da2.png) en klikt u op ![Pictogram tonen](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** handeling.

## Elementen gebruiken of plaatsen in eigen documenten {#place-assets-in-native-documents}

In sommige gevallen, bijvoorbeeld wanneer het plaatsen van activa in een inheems document, hebt u toegang tot een dossier in de Ontdekkingsreiziger van Vensters of de Vinder van MAC. Als u de locatie van het bestandssysteem van het lokaal gedownloade bestand wilt herstellen, gebruikt u de optie ![Pictogram onthullen](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**.

![File-actie onthullen voor een ](assets/revealfile_action_da2.png "assetReveal-actie voor een element")

Klik **[!UICONTROL Reveal File]**, of **[!UICONTROL Reveal Folder]** op een omslag, om de Ontdekkingsreiziger van Vensters of de Vinder van MAC met het dossier of de omslag te openen vooraf geselecteerd op uw lokale machine. De optie is nuttig om de [!DNL Experience Manager] dossiers in de inheemse toepassingen te plaatsen die het plaatsen of het verbinden van lokale dossiers steunen. Zie [Afbeeldingen plaatsen](https://helpx.adobe.com/indesign/using/placing-graphics.html) voor informatie over het plaatsen van bestanden in Adobe InDesign.

Met de handeling **[!UICONTROL Reveal File]** wordt een lokaal netwerkaandeel geopend. Hierin worden alleen de middelen weergegeven die lokaal beschikbaar zijn, dat wil zeggen de middelen die met de app zijn onthuld, gedownload of geopend/bewerkt. Het lokale netwerkaandeel uploadt geen veranderingen in [!DNL Experience Manager]. Als u de wijzigingen wilt uploaden, gebruikt u expliciet **[!UICONTROL Upload Changes]**- of **[!UICONTROL Upload]**-handelingen in de app.

>[!NOTE]
>
>Voor achterwaartse compatibiliteit met [!DNL Experience Manager] desktop app v1.x, worden de vrijgegeven bestanden aangeboden via een gedeeld lokaal netwerk, waarbij alleen lokaal beschikbare bestanden beschikbaar worden gemaakt. De bureaubladpaden van de onthulde bestanden zijn gelijk aan de paden die door app v1.x worden gemaakt.

>[!CAUTION]
>
>Gebruik de optie **[!UICONTROL Reveal File]** niet om elementen in native toepassingen te bewerken. Gebruik in plaats daarvan de handelingen **[!UICONTROL Edit]**. Zie [Geavanceerde workflow voor meer informatie: samenwerken aan dezelfde bestanden en bewerkingsconflicten vermijden](#adv-workflow-collaborate-avoid-conflicts).

## Elementen bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager] {#edit-assets-upload-updated-assets}

Open elementen die u wilt bewerken wanneer u wijzigingen wilt aanbrengen en upload de bijgewerkte elementen naar de AExExperience ManagerEM-server. U voorkomt conflicten met bewerkingen door andere gebruikers door met de app een bewerkingssessie te starten. Voordat u begint met bewerken, moet u ervoor zorgen dat er geen vergrendelingspictogram op het element staat, dat wil zeggen dat een andere gebruiker het element niet bewerkt.

Als u een element wilt bewerken, zoekt u het element of bladert u naar de locatie van het element. Klik ![Meer pictogram](assets/do-not-localize/more2_da2.png) en klik **[!UICONTROL Edit]**.

Gebruik **[!UICONTROL Toggle Check-out]** om het element te vergrendelen om conflicten te voorkomen met bewerkingen van andere gebruikers in beide volgende situaties:

* U hebt een middel bewerkt zonder het eerst uit te checken (bijvoorbeeld door het alleen te openen).
* U bent van plan binnenkort met het bewerken van een element te beginnen en wilt dat anderen dit niet bewerken.

Nadat u alle bewerkingen hebt uitgevoerd, geeft de app de status **[!UICONTROL Edited Locally]** weer voor de gewijzigde elementen. Alle wijzigingen die in de elementen zijn opgeslagen, zijn alleen lokaal totdat u de wijzigingen in [!DNL Experience Manager] uploadt. Als u een individu of een paar elementen een voor een wilt uploaden, klikt u op **[!UICONTROL Upload Changes]** uit de opties voor een element. Er wordt een versie van het element gemaakt in [!DNL Experience Manager]. Met behulp van de webinterface van [!DNL Assets] kunt u de elementgeschiedenis zien in de [tijdlijnweergave](https://experienceleague.adobe.com/docs/experience-manager-65/assets/using/activity-stream.html).

![De optie Wijzigingen uploaden in de ](assets/upload_changes_single1_da2.png "optie voor het uploaden van wijzigingen in de app")

![De optie Wijzigingen uploaden wanneer u een grote voorvertoning van een optie ](assets/upload_changes_single2_da2.png "voor het uploaden van middelen weergeeft wanneer u een grote voorvertoning van een element weergeeft")

Zie [Geavanceerde workflow voor beste werkwijzen over gezamenlijke bewerking: samenwerken aan dezelfde bestanden en bewerkingsconflicten vermijden](#adv-workflow-collaborate-avoid-conflicts).

In de volgende gevallen kunt u uw wijzigingen en bewerkingen in het lokale element negeren. Klik op **[!UICONTROL Discard Changes]**.

* Als u uw lokale wijzigingen niet wilt opslaan in [!DNL Experience Manager].
* Breng wijzigingen aan in het oorspronkelijke element nadat u enkele wijzigingen hebt opgeslagen.
* Bewerk het element niet meer omdat dit niet meer nodig is.

Schakel indien nodig het uitchecken in. Het bijgewerkte element wordt verwijderd uit de lokale cachemap en wordt opnieuw gedownload wanneer u het bewerkt of opent.

## Nieuwe elementen uploaden en toevoegen aan [!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

Gebruikers kunnen nieuwe elementen toevoegen aan de DAM-opslagplaats. U kunt bijvoorbeeld fotograaf of contractant zijn die een groot aantal foto&#39;s van een fotoshoot wil toevoegen aan de [!DNL Experience Manager]-opslagplaats. Als u nieuwe inhoud wilt toevoegen aan [!DNL Experience Manager], selecteert u ![Uploaden naar cloud-optie](assets/do-not-localize/upload_to_cloud_da2.png) in de bovenste balk van de app. Blader naar de elementbestanden in het lokale bestandssysteem en klik op **[!UICONTROL Select]**. U kunt ook elementen uploaden door de bestanden of mappen naar de toepassingsinterface te slepen. Als u in Windows elementen naar een map in de app sleept, worden de elementen naar de map geüpload. Als het langer duurt om te uploaden, geeft de app een voortgangsbalk weer.

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

U kunt mappen of afzonderlijke bestanden uploaden vanuit uw lokale bestandssysteem. De hiërarchie van een map blijft behouden wanneer deze wordt geüpload. Zie [Uploads bulksgewijs ](#bulk-upload-assets) voordat u elementen in bulk uploadt.

Als u de lijst met elementen wilt weergeven die in een bepaalde sessie zijn overgedragen, klikt u op **[!UICONTROL View]** > **[!UICONTROL Assets transfers]**. In de lijst kunt u de bestandsoverdrachten van de huidige sessie weergeven en snel verifiëren.

![Lijst van overgedragen elementen in een bepaalde ](assets/assets_transfered_da2.png "sessionList van overgedragen elementen in een bepaalde sessie")

U kunt de uploadsnelheid (versnelling) bepalen in **[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]**-instelling. Meer gelijktijdige uitvoering levert doorgaans snellere uploads op, maar kan ook bronintensief zijn en meer verwerkingskracht van de lokale machine verbruiken. Als u een traag systeem ervaart, uploadt u opnieuw met een lagere waarde voor gelijktijdige uitvoering.

>[!NOTE]
>
>De overdrachtlijst is niet blijvend en is niet beschikbaar als u de app afsluit en opnieuw opent.

### Speciale tekens in elementnamen beheren {#special-characters-in-filename}

In de verouderde app behielden de namen van knooppunten die in de repository zijn gemaakt de ruimten en behuizing van de mapnamen die door de gebruiker zijn verschaft. Schakel [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in [!UICONTROL Preferences] in als de huidige toepassing de regels voor nodenamen van v1.10-app moet emuleren. Zie [toepassingsvoorkeuren](/help/install-upgrade.md#set-preferences). Deze oudere voorkeur is standaard uitgeschakeld.

>[!NOTE]
>
>De app wijzigt alleen de knooppuntnamen in de repository met behulp van de volgende naamconventies. De app behoudt de `Title` van het element zoals deze is.

<!-- TBD: Do NOT use this table.

| Where do characters occur | Characters | Legacy preference | Renaming convention | Example |
|---|---|---|---|---|
| In file name extension | `.` | Enabled or disabled | Retained as is | NA |
| File or folder name | `. / : [ ] | *` | Enabled or disabled | Replaced with a `-` (hyphen) | `myimage.jpg` remains as is and `my.image.jpg` changes to `my-image.jpg`. |
| Folder name | `% ; # , + ? ^ { } "` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | `% # ? { } &` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Whitespaces | Enabled or disabled | Retained as is | NA |
| Folder name | Whitespaces | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Uppercase characters | Disabled | Retained as is | tbd |
| Folder name | Uppercase characters | Disabled | Replaced with a `-` (hyphen) | tbd |
-->

| Tekens ‡ | Oudere voorkeur in app | Wanneer voorkomen in bestandsnamen | Indien voorkomend in mapnamen | Voorbeeld |
|---|---|---|---|---|
| `. / : [ ] | *` | Ingeschakeld of Uitgeschakeld | Vervangen door `-` (afbreekstreepje). Een `.` (punt) in de bestandsnaamextensie blijft ongewijzigd. | Vervangen door `-` (afbreekstreepje). | `myimage.jpg` blijft ongewijzigd en  `my.image.jpg` verandert in  `my-image.jpg`. |
| `% ; # , + ? ^ { } "` en witruimte | ![deselecteren ](assets/do-not-localize/deselect-icon.png) iconDisabled | Werkruimten blijven behouden | Vervangen door `-` (afbreekstreepje). | `My Folder.` wijzigingen in  `my-folder-`. |
| `# % { } ? & .` | ![deselecteren ](assets/do-not-localize/deselect-icon.png) iconDisabled | Vervangen door `-` (afbreekstreepje). | NA. | `#My New File.` wijzigingen in  `-My New File-`. |
| Hoofdletters | ![deselecteren ](assets/do-not-localize/deselect-icon.png) iconDisabled | Trappen blijft ongewijzigd. | Veranderd in kleine letters. | `My New Folder` wijzigingen in  `my-new-folder`. |
| Hoofdletters | ![selectie gecontroleerd ](assets/do-not-localize/selection-checked-icon.png) iconEnabled | Trappen blijft ongewijzigd. | Trappen blijft ongewijzigd. | NA. |

‡ De lijst met tekens is een lijst met door spaties gescheiden tekens.

<!-- TBD: Check if the following is to be included in the footnote.

Do not use &#92;&#92; in the names of files and &#92;&#116; &#38; in the names of folders. 
-->


<!-- TBD: Securing the below presentation of the same content in a comment.

**File names**

| Characters | Replaced by |
|---|---|
| &#35; &#37; &#123; &#63; &#125; &#38; &#46; &#47; &#58; &#91; &#124; &#93; &#42; | hyphen (-) |
| whitespaces | whitespaces are retained |
| capital case | casing is retained |

>[!CAUTION]
>
>Avoid using &#92;&#92; in file names.

**Folder names**

| Characters | Replaced by |
|---|---|
| Characters | Replaced by |
| &#37; &#59; &#35; &#44; &#43; &#63; &#94; &#123; &#123; &#34; &#46; &#47; &#59; &#91; &#93; &#124; &#42; | hyphen (-) |
| whitespaces | hyphen (-) |
| capital case | lower case |

>[!CAUTION]
>
>Avoid using &#92;&#92; &#92;&#116; &#38; in folder names.

>[!NOTE]
>
>If you enable [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in app [!UICONTROL Preferences], then the app emulates v1.10 app behavior when uploading folders. In v1.10, the node names created in the repository respect spaces and casing of the folder names provided by the user. For more information, see [app Preferences](/help/install-upgrade.md#set-preferences).

-->

## Werken met meerdere elementen {#work-with-multiple-assets}

Gebruikers kunnen eenvoudig met meerdere elementen werken en deze beheren door bijvoorbeeld alle bewerkingen in één keer te uploaden of geneste mappen met een paar klikken te uploaden.

### Door grote mappen bladeren {#browse-large-folders}

Als u werkt met mappen die veel elementen bevatten, schuift u om meer elementen weer te geven. Als u met het toetsenbord wilt schuiven, drukt u een paar keer op Tab om het element aan de bovenkant te selecteren. Let op het gemarkeerde element om te weten wanneer het is geselecteerd. Gebruik nu de toets Pijl-omlaag om door de lijst met elementen te gaan.

### Snelle handelingen voor geselecteerde elementen {#quick-actions-for-selected-assets}

Klik op de miniatuur van een paar elementen om de elementen te selecteren. Als u alle elementen wilt selecteren, klikt u op het selectievakje in de bovenste balk van de app. De set handelingen die van toepassing is op alle geselecteerde elementen samen worden weergegeven op een werkbalk onder aan de app.

![De werkbalk onder aan geeft acties weer die relevant zijn voor de geselecteerde ](assets/actions_bottom_toolbar1_da2.png "elementen. De werkbalk onder aan het venster toont algemene acties voor de geselecteerde elementen")

![Geen acties op de werkbalk als er geen gemeenschappelijke acties voor de ](assets/actions_bottom_toolbar2_da2.png "selectie zijnGeen acties op de werkbalk als er geen gemeenschappelijke acties voor de selectie zijn")

Welke acties beschikbaar zijn op de werkbalk onderaan, is afhankelijk van de status van de geselecteerde bestanden. Als u bijvoorbeeld alleen **[!UICONTROL Edited Locally]** bestanden selecteert, wordt **[!UICONTROL Upload Changes]** pictogram weergegeven. Als u een combinatie van **[!UICONTROL Edited locally]** en **[!UICONTROL Cloud only]** selecteert, is de **[!UICONTROL Upload Changes]** actie niet beschikbaar.

### Alle bewerkte afbeeldingen zoeken {#find-all-edited-images}

De toepassing biedt een weergave met de naam **[!UICONTROL Edited locally]**, waarmee u snel toegang krijgt tot alle bestanden die u lokaal hebt gedownload (via de acties [!UICONTROL Open] of [!UICONTROL Edit]) en vervolgens hebt gewijzigd. Met de app kunt u alle lokaal bewerkte elementen selecteren en de wijzigingen met een paar klikken uploaden. In deze weergave worden ook de lokaal bewerkte elementen weergegeven die een bewerkingsconflict hebben.

![Filter om alle lokaal bewerkte ](assets/edited_locally_filter_da2.png "assetsFilter te bekijken om alle lokaal bewerkte middelen te zien, bijvoorbeeld voor het bulkuploaden van bewerkingen")

### Bulkupload-elementen {#bulk-upload-assets}

Gebruikers of organisaties, zoals fotografen of creatieve bureaus, kunnen in scenario&#39;s een groot aantal lokale elementen maken, zoals foto&#39;s, retoucheren of selectie uit een grotere set die buiten [!DNL Experience Manager] wordt uitgevoerd. Ze kunnen deze grote lokale mappen rechtstreeks vanuit de bureaubladtoepassing uploaden naar [!DNL Assets]. De maphiërarchieën blijven behouden en alle geneste submappen en opgenomen elementen worden geüpload. De geüploade elementen zijn direct ook beschikbaar voor andere gebruikers van dezelfde server. Elementen worden op de achtergrond geüpload, dus de bewerking is niet gekoppeld aan een webbrowsersessie.

![Met Bulk kunt u meerdere lokale mappen vanaf uw bureaublad uploaden naar  [!DNL Experience Manager]](assets/upload_local_folders_da2.png "Bulksgewijs meerdere lokale mappen vanaf uw bureaublad naar de Experience Manager")

Als na het uploaden de verwachte wijzigingen niet worden doorgevoerd in de app, klikt u op het pictogram Vernieuwen ![Vernieuwen](assets/do-not-localize/refresh.png).

>[!NOTE]
>
>Gebruik geen uploadfunctionaliteit om elementen over twee [!DNL Experience Manager] implementaties te migreren. Zie in plaats daarvan de [migratiegids](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/assets-migration-guide.html).

### Lijst van overgedragen elementen {#list-of-transferred-assets}

Zie [Elementen uploaden naar [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem) voor een overzicht van de elementen die in een bepaalde sessie zijn overgedragen.

## Geavanceerde workflow: begin van de [!DNL Assets] Webinterface {#adv-workflow-start-from-aem-ui}

Start zo nodig uw workflow via de webinterface Middelen. De bureaubladtoepassing integreert met de [!DNL Experience Manager] om op verzoek over te nemen met behulp van desktophandelingen.

Een bijzonder geval van het beginnen van werkschema van de Webinterface is middelenontdekking. De gebruikersinterface van de Omnissearch bar in Assets biedt een rijke en geavanceerde zoekervaring. U wilt mogelijk eerst een gewenst middel zoeken op het web en vervolgens de workflow in de app starten met [!UICONTROL Desktop Actions]. Sommige voorbeeldgevallen zijn het filteren van zoekresultaten met gebruik van facetten, het zoeken naar een specifiek middel waarvoor een licentie is verleend door Adobe Stock of een aanpassing die door uw organisatie is geïmplementeerd waardoor u een betere detectie kunt uitvoeren via de webinterface.

De functionaliteit van de bureaubladtoepassing wordt gebruikt wanneer u de volgende handelingen uitvoert in de webinterface Middelen:

* De [!UICONTROL Desktop Actions] die [!UICONTROL Open], [!UICONTROL Edit], en [!UICONTROL Reveal] toestaat
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] or [!UICONTROL check-in]

De acties in de webinterface die beschikbaar zijn voor een element dat is uitgecheckt in de app zijn bijvoorbeeld [!UICONTROL Open], [!UICONTROL Reveal] en [!UICONTROL Check-in].

![Bureaubladhandelingen in de  [!DNL Experience Manager] webinterface:](assets/assets_web_actions_da2.png "Desktophandelingen in de webinterface van Experience Manager")

>[!NOTE]
>
>Mogelijk wordt u door de browser gevraagd om het starten van [!DNL Adobe Experience Manager] Desktop toe te staan. Als u wilt genieten van een ononderbroken overdracht van de browser naar de app, schakelt u het desbetreffende selectievakje in zodat de app altijd overneemt.

U kunt de volgende informatie of workflow niet vinden met de webinterface. Gebruik de bureaubladtoepassing omdat de webinterface lokale wijzigingen niet bijhoudt en zich niet bewust is van het volgende:

* Bestanden die lokaal zijn bewerkt.
* Bestanden met een bewerkingsconflict en een manier om dit op te lossen.
* Lokale wijzigingen uploaden naar [!DNL Experience Manager].
* Verschillende statussen van de lokaal beschikbare bestanden.

Integendeel, u kunt het element in de webinterface openen vanaf de bureaubladtoepassing met de actie **[!UICONTROL Open In Web]**.

## Geavanceerde workflow: samenwerken aan dezelfde bestanden en bewerkingsconflicten voorkomen {#adv-workflow-collaborate-avoid-conflicts}

In samenwerkingsomgevingen kunnen meerdere gebruikers werken aan dezelfde set elementen die tot versieconflicten kunnen leiden. Volg de volgende aanbevolen procedures om conflicten te voorkomen:

* Bewerk geen elementen door op [!UICONTROL Open] te klikken. Bewerk de lokaal gedownloade elementen niet door deze te openen vanuit de bestandssysteemmap. Andere gebruikers weten niet dat het element wordt bewerkt.
* Als u een element wilt bewerken, klikt u altijd op [!UICONTROL Edit]. Het element wordt geopend in de oorspronkelijke toepassing en er wordt een vergrendelingspictogram toegevoegd aan het element, zodat de andere gebruikers weten dat het element wordt bewerkt.
* Klik [!UICONTROL Toggle Check-in] als u per ongeluk begint te uitgeven zonder [!UICONTROL Edit] te klikken. Hiermee voegt u een vergrendelingspictogram toe aan het element. Zelfs als u een element later wilt bewerken, maar u wilt voorkomen dat anderen het bewerken, klikt u op [!UICONTROL Toggle Check-in] om het element te vergrendelen.
* Voordat u een element bewerkt, moet u ervoor zorgen dat andere gebruikers het element niet bewerken. Zoek het slotpictogram op de activa.
* Na het voltooien van de bewerkingen uploadt u alle wijzigingen en checkt u het element in.

![Status van het bewerken van ](assets/edits_conflicts_status_da2.png "conflictenStatus van het bewerken van conflicten")

Als een lokaal gedownload element wordt bijgewerkt op de [!DNL Experience Manager]-server, geeft de app de status **[!UICONTROL Modified remotely]** weer. U kunt uw lokale kopie verwijderen of de lokale kopie vernieuwen door respectievelijk [!UICONTROL Remove] of [!UICONTROL Update] te klikken. Via koppelingen in het dialoogvenster kunt u beide versies van het element weergeven.

![Opties om het conflict op te lossen wanneer het element op afstand wordt ](assets/modified_remotely_dialog_da2.png "gewijzigdOpties om het conflict op te lossen wanneer het element op afstand wordt gewijzigd")

Als een middel dat u lokaal bewerkt ook zonder uw medeweten op de server wordt bijgewerkt, geeft de app een **[!UICONTROL Editing Conflict]**-status weer. U kunt één set van de wijzigingen behouden - ofwel uw updates behouden (klik op **[!UICONTROL Keep Mine]**) en de bewerking van de andere gebruiker verwijderen, of de updates van de andere gebruiker respecteren en uw wijzigingen verwijderen (**[!UICONTROL Overwrite Mine]**).

![Opties voor het oplossen van een bewerkingsconflictOpties voor het oplossen van een bewerkingsconflict ](assets/editing_conflict_dialog_da2.png "")

## Geavanceerde workflow: elementen plaatsen en koppelen in InDesign-bestand {#adv-workflow-place-assets-indesign}

Wanneer u de [!DNL Experience Manager]-bureaubladtoepassing gebruikt om bestanden met gekoppelde elementen te openen, worden de elementen vooraf gedownload en in de oorspronkelijke toepassingen geplaatst. Deze workflow werkt alleen als uw oorspronkelijke toepassing ondersteuning biedt voor het plaatsen van koppelingen naar lokale elementen. [!DNL Experience Manager] moet ondersteuning bieden voor het oplossen van deze koppelingen in binaire bestanden naar verwijzingen naar de server.

[!DNL Experience Manager] De bureaubladtoepassing ondersteunt deze workflow met een aantal geselecteerde Adobe Creative Cloud-bureaubladtoepassingen en -bestandsindelingen: Adobe InDesign, Adobe Illustrator en Adobe Photoshop. Met de workflow kunt u efficiënt werken met de ondersteunde Creative Cloud-bestanden. Dus als gebruiker A een paar elementen in een InDesign-bestand plaatst en dit bestand in [!DNL Experience Manager] controleert, ziet gebruiker B de elementen in het InDesign-bestand, ook al maken de elementen geen deel uit van het bestand. De middelen worden plaatselijk gedownload op de machine van gebruiker B.

>[!NOTE]
>
>De bureaubladtoepassing kan worden toegewezen aan elk station in Windows. Wijzig de standaardstationsletter echter niet voor vloeiende bewerkingen. Als gebruikers van dezelfde organisatie verschillende stationsletters gebruiken, kunnen ze de elementen die door anderen zijn geplaatst, niet zien. De geplaatste elementen worden niet opgehaald wanneer het pad verandert. De geplaatste elementen blijven in het binaire bestand (bijvoorbeeld INDD) staan en worden niet verwijderd.

Zie de [systeemvereisten en de ondersteunde versies](release-notes.md) voor informatie over de beperkingen van deze workflow.

Voer de volgende stappen uit om deze workflow te testen met een afbeeldingselement en InDesign:

1. Behoud handig een INDD-bestand met geplaatste elementen in [!DNL Experience Manager]. Zie [Afbeeldingen plaatsen](https://helpx.adobe.com/indesign/using/placing-graphics.html) voor informatie over het maken van een dergelijk INDD-bestand.
1. Vanuit de bureaubladtoepassing **[!UICONTROL Edit]** het INDD-bestand met elementen die in [!DNL Experience Manager] zijn geplaatst.
1. De app downloadt zowel het InDesign-bestand als de gekoppelde elementen. Wanneer InDesign het document opent, worden de koppelingen opgelost, worden de elementen gedownload en worden de elementen weergegeven in het InDesign-document.
1. Als u een nieuwe afbeelding in het InDesign-bestand wilt plaatsen, gebruikt u de handeling **[!UICONTROL Reveal File]** op het element. De actie downloadt plaatselijk activa en opent de lokale plaats van het netwerkaandeel in de Ontdekkingsreiziger van Vensters of de Vinder van MAC.
1. Plaats het onthulde element in het InDesign-document. Hiermee maakt u een koppeling in het document.
1. Nadat u de bewerkingen in het InDesign-document hebt voltooid, slaat u het document op en uploadt u het naar [!DNL Experience Manager] met de bureaubladtoepassing.

## Geavanceerde workflow: de elementen lokaal downloaden {#adv-workflow-download-assets-locally}

De toepassing downloadt de middelen van [!DNL Experience Manager] server plaatselijk op uw dossiersysteem in vele scenario&#39;s. De downloads verbruiken bandbreedte en schijfruimte. Als u de scenario&#39;s kent, kunt u de wachttijd tot de downloads zijn voltooid, optimaliseren.

U kunt de middelen downloaden vanuit de app op aanvraag. Zie [Elementen downloaden](#download-assets).

Wanneer u de handeling [!UICONTROL Open] gebruikt om middelen te openen in een native desktoptoepassing, wordt het middel lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [Elementen openen](#openondesktop-v2).

Wanneer u de locatie van een middel of een map vanuit de app weergeeft, wordt het middel of de map eerst lokaal gedownload en vervolgens op uw computer geopend in het gedeelde lokale netwerk. Zie [Elementen openen](#openondesktop-v2).

Wanneer u de handeling [!UICONTROL Edit] gebruikt om middelen in een native desktoptoepassing te bewerken, wordt het middel lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [Elementen bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager]](#edit-assets-upload-updated-assets).

Als de toepassing is geïnstalleerd en toegestaan, worden de handelingen voltooid wanneer u [!UICONTROL Desktop Actions] van [!DNL Experience Manager] webinterface gebruikt. De app downloadt het middel eerst en voltooit de actie.
