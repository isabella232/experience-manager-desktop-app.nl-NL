---
title: Gebruiken [!DNL Experience Manager] bureaubladtoepassing
description: Gebruiken [!DNL Adobe Experience Manager] bureaubladtoepassing, voor gebruik met [!DNL Adobe Experience Manager] DAM-middelen worden direct vanaf uw Win- of Mac-desktop gebruikt in andere toepassingen.
mini-toc-levels: 1
feature: Desktop App,Asset Management
exl-id: fa19d819-231a-4a01-bfd2-6bba6fec2f18
source-git-commit: ca04b64e1ebfee4b677fcc5ef84b0e8fd9950d17
workflow-type: tm+mt
source-wordcount: '4054'
ht-degree: 0%

---

# Gebruiken [!DNL Adobe Experience Manager] bureaubladtoepassing {#use-aem-desktop-app-v2}

Gebruik de [!DNL Adobe Experience Manager] bureaubladtoepassing, voor eenvoudige toegang tot de digitale middelen die zijn opgeslagen in [!DNL Adobe Experience Manager] DAM-opslagplaats op uw lokale bureaublad en gebruik deze middelen in bureaubladtoepassingen. U kunt de middelen in Desktoptoepassingen openen en de activa plaatselijk uitgeven - upload de veranderingen terug naar [!DNL Experience Manager] met versiebeheer, om de updates met andere gebruikers te delen. U kunt ook nieuwe bestanden en maphiërarchieën uploaden naar [!DNL Experience Manager], mappen maken en elementen of mappen verwijderen uit [!DNL Experience Manager] DAM.

Dankzij de integratie kunnen verschillende rollen in de organisatie de elementen centraal beheren in [!DNL Experience Manager Assets] en toegang te krijgen tot de middelen op het lokale bureaublad in de native toepassingen op Windows of Mac OS.

Wanneer u de toepassing opent nadat u zich hebt afgemeld of voor het eerst, geeft u de URL van de toepassing op [!DNL Experience Manager] server in de indeling `https://[aem-server-url]:[port]/`. Selecteer vervolgens de [!UICONTROL Connect] optie. Geef referenties op om de toepassing te verbinden met de server.

De belangrijkste taken u uitvoert gebruikend [!DNL Adobe Experience Manager] desktop-app is:

![Workflows en taken die u kunt uitvoeren [!DNL Experience Manager] bureaubladtoepassing](assets/aem_desktop_app_usecases_v2.png "Workflows en taken die u kunt uitvoeren [!DNL Adobe Experience Manager] bureaubladtoepassing")
Downloaden [dit](assets/aem_desktop_app_usecases_print.pdf) afdrukklaar PDF-bestand.

## Hoe desktop app werkt {#how-app-works2}

Begrijp voordat u de toepassing gaat gebruiken [De werking van de app](release-notes.md#how-app-works). Zorg ook dat u bekend bent met de volgende termen:

* **[!UICONTROL Desktop Actions]**: Vanuit de webinterface Middelen kunt u vanuit een browser de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw native desktoptoepassing. Deze acties zijn beschikbaar via de webinterface en gebruiken de functionaliteit van de bureaubladtoepassing. Zie [hoe u desktophandelingen kunt inschakelen](using.md#desktopactions-v2).

* Bestandsstatus is **[!UICONTROL Cloud Only]**: Dergelijke middelen zijn niet gedownload op de lokale computer en zijn beschikbaar op [!DNL Experience Manager] alleen server.

* Bestandsstatus is **[!UICONTROL Available locally]**: De middelen worden gedownload en beschikbaar op de lokale computer zoals is. De elementen worden niet gewijzigd.

* Bestandsstatus is **[!UICONTROL Edited locally]**: Dergelijke elementen worden lokaal gewijzigd en de wijzigingen blijven van toepassing op de bestanden die worden geüpload naar [!DNL Experience Manager] server. Nadat u het uploadt, verandert de status in [!UICONTROL Available locally]. Zie [elementen bewerken](using.md#edit-assets-upload-updated-assets).

* Bestandsstatus is **[!UICONTROL Editing conflict]**: Als u en andere gebruikers tegelijkertijd een element wijzigen, geeft de app aan dat er een bewerkingsconflict is opgetreden. De app biedt ook opties om uw wijzigingen te behouden of te negeren. Zie [hoe te vermijden het uitgeven conflicten](using.md#adv-workflow-collaborate-avoid-conflicts).

* Bestandsstatus is **[!UICONTROL Modified remotely]**: In de app wordt aangegeven of een element dat u hebt gedownload, is gewijzigd op het tabblad [!DNL Experience Manager] server. De app biedt ook de optie om de nieuwste versie te downloaden en uw lokale kopie bij te werken. Zie [hoe te vermijden het uitgeven conflicten](using.md#adv-workflow-collaborate-avoid-conflicts).

* **[!UICONTROL Check-out]**: Als u een bestand bewerkt of van plan bent een bestand te bewerken, schakelt u de status in of uit. Er wordt een vergrendelingspictogram toegevoegd aan het middel in de app en [!DNL Experience Manager] webinterface. Met het vergrendelingspictogram kunnen andere gebruikers voorkomen dat hetzelfde element tegelijk wordt bewerkt, omdat dit tot een bewerkingsconflict leidt.

* **[!UICONTROL Check-in]**: Markeer het element als veilig voor andere gebruikers om het te bewerken zonder een bewerkingsconflict te veroorzaken. Wanneer u uw wijzigingen uploadt, wordt het vergrendelingspictogram automatisch verwijderd. Als u de incheck-status inschakelt, wordt ook het vergrendelingspictogram verwijderd. U wordt echter aangeraden dit niet handmatig in te checken zonder de wijzigingen te uploaden. Als u de wijzigingen verwijdert, schakelt u het inchecken handmatig in of uit.

* **[!UICONTROL Open]** handeling: Open gewoon het element om er een voorvertoning van weer te geven in de oorspronkelijke toepassing. Het wordt afgeraden het element met deze handeling te bewerken, omdat het element niet wordt uitgecheckt en andere gebruikers bewerkingen kunnen uitvoeren die tot bewerkingsconflicten leiden.

* **[!UICONTROL Edit]** handeling: Gebruik de handeling om de afbeelding te wijzigen. Klikken [!UICONTROL Edit] Hiermee wordt het element automatisch uitgecheckt en wordt een vergrendelingspictogram toegevoegd aan het element. Klik op Bewerken als u het element niet wilt bewerken en klik vervolgens op [!UICONTROL Toggle check-in]. Elementen verwijderen, hernoemen of verplaatsen in [!DNL Experience Manager] DAM-maphiërarchie, gebruik de [!DNL Experience Manager] Webinterfaceacties en niet de bewerkingshandeling.

* **[!UICONTROL Download]** handeling: Download het middel naar uw lokale computer. U kunt de elementen nu downloaden en later bewerken. werk offline en upload de wijzigingen later. Elementen worden gedownload in een cachemap op uw bestandssysteem.

* **[!UICONTROL Reveal File]** of **[!UICONTROL Reveal Folder]** handeling: Terwijl de elementen naar een lokale cachemap worden gedownload, bootst de toepassing een lokale netwerkschijf na en biedt deze een lokaal pad voor elk element. Als u dit pad wilt weten, gebruikt u de desbetreffende openingsoptie in de app. U moet actie onthullen om elementen in de Creative Cloud-toepassing te plaatsen. Zie [elementen plaatsen](using.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]** handeling: Het element weergeven in [!DNL Experience Manager] webinterface, opent u deze in het web. U kunt meer workflows starten vanuit [!DNL Experience Manager] interface zoals het bijwerken van metagegevens of het detecteren van elementen.

* **[!UICONTROL Delete]** handeling: Het element verwijderen uit de [!DNL Experience Manager] DAM-opslagplaats. De actie schrapt de originele kopie van het middel op de server van de Experience Manager. Als u wijzigingen in het lokale element alleen wilt negeren, raadpleegt u [wijzigingen negeren](using.md#edit-assets-upload-updated-assets).

* **[!UICONTROL Upload Changes]**: De bureaubladtoepassing uploadt het bijgewerkte element alleen wanneer u het expliciet uploadt naar [!DNL Experience Manager] server. Wanneer u uw bewerkingen opslaat, worden de wijzigingen alleen op uw lokale computer opgeslagen. Tijdens het uploaden wordt het element automatisch ingecheckt en wordt het vergrendelingspictogram verwijderd. Zie [elementen bewerken](using.md#edit-assets-upload-updated-assets).

## Bureaubladhandelingen inschakelen in [!DNL Experience Manager] webinterface {#desktopactions-v2}

Van binnen [!DNL Assets] in een browser, kunt u de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw desktoptoepassing. Deze opties worden [!UICONTROL Desktop Actions] en zijn niet standaard ingeschakeld. Voer de volgende stappen uit om deze functie in te schakelen.

1. In de [!DNL Assets] console, klik **[!UICONTROL User]** op de werkbalk.
1. Klikken **[!UICONTROL My Preferences]** om de **[!UICONTROL Preferences]** .

1. In de [!UICONTROL User Preferences] dialoogvenster, selecteren **[!UICONTROL Show Desktop Actions For Assets]** en klik vervolgens op **[!UICONTROL Accept]**.


   ![Selecteer Bureaubladhandelingen weergeven voor elementen om bureaubladhandelingen in te schakelen](assets/enable_desktop_actions.png)

   *Afbeelding: Selecteren [!UICONTROL Show Desktop Actions For Assets] om bureaubladhandelingen in te schakelen.*

## Zoeken, zoeken en voorvertonen van elementen {#browse-search-preview-assets}

U kunt naar de elementen bladeren die beschikbaar zijn in het dialoogvenster [!DNL Experience Manager] opslagplaats, allemaal vanuit de bureaubladtoepassing. Probeer het volgende in de app:

1. Blader naar een map en bekijk basisinformatie over de middelen die beschikbaar zijn in de map, samen met kleine miniaturen van alle elementen.

   ![Door de DAM-bestanden en -mappen bladeren](assets/browse_folder_da2.png "Door de DAM-bestanden en -mappen bladeren")

1. Klik op de bestandsnaam als u meer informatie en een grotere miniatuur van een afzonderlijk element wilt bekijken.

   ![Een grotere voorvertoning van een element en handelingen bekijken](assets/large_preview_actions_da2.png "Een grotere voorvertoning van een element en handelingen bekijken")

1. Klikken **[!UICONTROL Open]** of **[!UICONTROL Edit]** om het bestand lokaal te downloaden en het alleen weer te geven of te bewerken in respectievelijk de oorspronkelijke toepassing.
1. Zoeken met trefwoorden om een verwant element te zoeken in het dialoogvenster [!DNL Experience Manager] opslagplaats. Gebruiken `?` en `*` als jokertekens. Deze jokertekens vervangen een enkel teken of meerdere tekens. Filter de resultaten en sorteer deze zo nodig.

   ![Voorbeeld van zoeken met jokerteken voor sterretjes](assets/search_wildcard_da2.png "Voorbeeld van zoeken met jokerteken voor sterretjes")

   ![Een andere voorbeeldzoekopdracht met jokerteken voor sterretjes](assets/search_wildcard2_da2.png "Een andere voorbeeldzoekopdracht met andere plaatsing van het jokerteken voor sterretjes")

>[!NOTE]
>
>In de app worden de elementen weergegeven door de zoekcriteria af te stemmen op meerdere metagegevensvelden en niet alleen op de titel van het element of de bestandsnaam.

## Elementen downloaden {#download-assets}

U kunt de elementen downloaden naar uw lokale bestandssysteem. De app haalt de middelen op van [!DNL Experience Manager] en slaat dezelfde kopie op uw lokale bestandssysteem op.

Klikken ![Pictogram Meer opties](assets/do-not-localize/more2_da2.png) voor opties en klik op ![Downloadpictogram](assets/do-not-localize/download_cloud_da2.png) om te downloaden.

![Downloadoptie voor een element](assets/download_option_da2.png "Downloadoptie voor een element")

>[!NOTE]
>
>Wanneer u een groot bestand of een groot aantal bestanden downloadt of uploadt, schakelt de toepassing de handelingen voor elementen en mappen uit. De acties zijn beschikbaar wanneer het downloaden of uploaden is voltooid.

Het downloaden van meerdere elementen kan leiden tot slechte prestaties als de wachtrij groot is of als u te maken krijgt met een netwerkprobleem. Het is ook onbekend dat u veel bestanden in de wachtrij plaatst om te downloaden wanneer u een map downloadt. Om lange wachttijden te vermijden, beperkt app het aantal elementen dat in één keer wordt gedownload. Om te weten hoe te om het te vormen, zie [Voorkeuren instellen](install-upgrade.md#set-preferences). Zelfs onder deze limiet kan de app soms om bevestiging vragen voordat een ogenschijnlijk grote map wordt gedownload.

![App bevestigt download van relatief groot aantal elementen](assets/download_confirmation_da2.png "App bevestigt download van relatief groot aantal elementen")

Als er mappen zijn geselecteerd en gedownload, downloadt de toepassing alleen elementen die rechtstreeks in de map(pen) in [!DNL Experience Manager]. Elementen worden niet automatisch uit submappen gedownload.

## Elementen op uw bureaublad openen {#openondesktop-v2}

U kunt de externe middelen openen voor weergave in de oorspronkelijke toepassing. De middelen worden gedownload aan een lokale omslag en gelanceerd in de inheemse toepassing verbonden aan het dossierformaat. U kunt de oorspronkelijke toepassing wijzigen en specifieke bestandstypen (extensies) openen in uw Mac of Windows.

Klikken **[!UICONTROL Open]** in het menu Middelen. Het element wordt lokaal gedownload en in de oorspronkelijke toepassing geopend. Controleer de voortgang van het downloaden en de overdrachtssnelheid van grote middelen op de statusbalk.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>Als de verwachte wijzigingen niet worden doorgevoerd in de app, klikt u op het pictogram Vernieuwen ![Pictogram Vernieuwen](assets/do-not-localize/refresh.png) of klik met de rechtermuisknop in de toepassingsinterface en klik op **[!UICONTROL Refresh]**. De acties zijn niet beschikbaar wanneer grotere downloads of uploads worden uitgevoerd.

Als u de lokale downloadmap van een element wilt openen, klikt u op ![Pictogram Meer handelingen](assets/do-not-localize/more2_da2.png) en klik op ![Pictogram Tonen](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** handeling.

## Elementen gebruiken of plaatsen in eigen documenten {#place-assets-in-native-documents}

In sommige gevallen, bijvoorbeeld wanneer het plaatsen van activa in een inheems document, hebt u toegang tot een dossier in de Ontdekkingsreiziger van Vensters of de Vinder van Mac. Als u naar de locatie van het bestandssysteem wilt gaan waar het lokaal gedownloade bestand zich bevindt, gebruikt u de opdracht ![Pictogram Tonen](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** optie.

![Bestandsactie tonen voor een element](assets/revealfile_action_da2.png "Bestandsactie tonen voor een element")

Klikken **[!UICONTROL Reveal File]**, of **[!UICONTROL Reveal Folder]** in een map, om Windows Verkenner of de Finder van Mac te openen met het bestand of de map die vooraf op uw lokale computer is geselecteerd. De optie is handig om bijvoorbeeld de optie [!DNL Experience Manager] bestanden in de native toepassingen die het plaatsen of koppelen van lokale bestanden ondersteunen. Zie voor informatie over het plaatsen van bestanden in Adobe InDesign [Afbeeldingen plaatsen](https://helpx.adobe.com/indesign/using/placing-graphics.html).

De **[!UICONTROL Reveal File]** Met deze handeling wordt een lokaal gedeelde netwerk geopend, dat alleen de elementen weergeeft die lokaal beschikbaar zijn. Er worden dus elementen weergegeven die met de app zijn onthuld, gedownload of geopend/bewerkt. Het lokale netwerkaandeel uploadt geen veranderingen in [!DNL Experience Manager]. Om de veranderingen te uploaden, uitdrukkelijk gebruik **[!UICONTROL Upload Changes]** of **[!UICONTROL Upload]** acties in de app.

>[!NOTE]
>
>Voor achterwaartse compatibiliteit met [!DNL Experience Manager] bureaubladtoepassing v1.x, de bestanden die worden weergegeven, worden via een lokaal gedeeld netwerk aangeboden, waarbij alleen lokaal beschikbare bestanden beschikbaar worden gemaakt. De bureaubladpaden van de onthulde bestanden zijn gelijk aan de paden die door app v1.x worden gemaakt.

>[!CAUTION]
>
>Niet gebruiken **[!UICONTROL Reveal File]** om elementen in native toepassingen te bewerken. Gebruik in plaats daarvan de **[!UICONTROL Edit]** handelingen. Zie voor meer informatie [Geavanceerde workflow: samenwerken aan dezelfde bestanden en bewerkingsconflicten voorkomen](#adv-workflow-collaborate-avoid-conflicts).

## Elementen bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager] {#edit-assets-upload-updated-assets}

Open elementen die u wilt bewerken wanneer u wijzigingen wilt aanbrengen en upload de bijgewerkte elementen naar de AExExperience ManagerEM-server. U voorkomt conflicten met bewerkingen door andere gebruikers door met de app een bewerkingssessie te starten. Voordat u begint met bewerken, moet u ervoor zorgen dat er geen vergrendelingspictogram op het element staat, dat wil zeggen dat een andere gebruiker het element niet bewerkt.

Als u een element wilt bewerken, zoekt u het element of bladert u naar de locatie van het element. Klikken ![Meer pictogram](assets/do-not-localize/more2_da2.png) en klik op **[!UICONTROL Edit]**.

Gebruiken **[!UICONTROL Toggle Check-out]** het element vergrendelen om conflicten te voorkomen met bewerkingen van andere gebruikers in beide volgende situaties:

* U hebt een middel bewerkt zonder het eerst uit te checken (bijvoorbeeld door het alleen te openen).
* U bent van plan binnenkort met het bewerken van een element te beginnen en wilt dat anderen dit niet bewerken.

Nadat u de bewerkingen hebt uitgevoerd, wordt in de app het dialoogvenster **[!UICONTROL Edited Locally]** status voor de gewijzigde elementen. Alle wijzigingen die in de elementen zijn opgeslagen, zijn alleen lokaal totdat u de wijzigingen uploadt naar [!DNL Experience Manager]. Als u een individu of een paar elementen een voor een wilt uploaden, klikt u op **[!UICONTROL Upload Changes]** uit de opties voor een element. Er wordt een versie van het element gemaakt in [!DNL Experience Manager]. De webinterface gebruiken van [!DNL Assets]kunt u de geschiedenis van elementen in de [Tijdlijnweergave](https://experienceleague.adobe.com/docs/experience-manager-65/assets/using/activity-stream.html).

![De optie Wijzigingen uploaden in de app](assets/upload_changes_single1_da2.png "De optie Wijzigingen uploaden in de app")

![De optie Wijzigingen uploaden bij weergave van een grote voorvertoning van een element](assets/upload_changes_single2_da2.png "De optie Wijzigingen uploaden bij weergave van een grote voorvertoning van een element")

Voor beste praktijken rond samenwerkings het uitgeven, zie [Geavanceerde workflow: samenwerken aan dezelfde bestanden en bewerkingsconflicten voorkomen](#adv-workflow-collaborate-avoid-conflicts).

In de volgende gevallen kunt u uw wijzigingen en bewerkingen in het lokale element negeren. Klik op **[!UICONTROL Discard Changes]**.

* Als u uw lokale wijzigingen niet wilt opslaan in [!DNL Experience Manager].
* Breng wijzigingen aan in het oorspronkelijke element nadat u enkele wijzigingen hebt opgeslagen.
* Bewerk het element niet meer omdat dit niet meer nodig is.

Schakel indien nodig het uitchecken in. Het bijgewerkte element wordt verwijderd uit de lokale cachemap en wordt opnieuw gedownload wanneer u het bewerkt of opent.

## Nieuwe elementen uploaden en toevoegen aan [!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

Gebruikers kunnen nieuwe elementen toevoegen aan de DAM-opslagplaats. U kunt bijvoorbeeld een fotograaf of contractant zijn die een groot aantal foto&#39;s van een foto aan de [!DNL Experience Manager] opslagplaats. Nieuwe inhoud toevoegen aan [!DNL Experience Manager], selecteert u ![uploaden naar cloud, optie](assets/do-not-localize/upload_to_cloud_da2.png) in de bovenste balk van de app. Blader naar de elementbestanden in het lokale bestandssysteem en klik op **[!UICONTROL Select]**. U kunt ook elementen uploaden door de bestanden of mappen naar de toepassingsinterface te slepen. Als u in Windows elementen naar een map in de app sleept, worden de elementen naar de map geüpload. Als het langer duurt om te uploaden, geeft de app een voortgangsbalk weer.

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

U kunt mappen of afzonderlijke bestanden uploaden vanuit uw lokale bestandssysteem. De hiërarchie van een map blijft behouden wanneer deze wordt geüpload. Voordat u elementen in bulk uploadt, raadpleegt u [Bulkuploads](#bulk-upload-assets).

Klik op **[!UICONTROL View]** > **[!UICONTROL Assets transfers]**. In de lijst kunt u de bestandsoverdrachten van de huidige sessie weergeven en snel verifiëren.

![Lijst met overgedragen elementen in een bepaalde sessie](assets/assets_transfered_da2.png "Lijst met overgedragen elementen in een bepaalde sessie")

U kunt de uploadsnelheid (versnelling) bepalen in **[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]** instellen. Meer gelijktijdige uitvoering levert doorgaans snellere uploads op, maar kan ook bronintensief zijn en meer verwerkingskracht van de lokale machine verbruiken. Als u een traag systeem ervaart, uploadt u opnieuw met een lagere waarde voor gelijktijdige uitvoering.

>[!NOTE]
>
>De overdrachtlijst is niet blijvend en is niet beschikbaar als u de app afsluit en opnieuw opent.

### Speciale tekens in elementnamen beheren {#special-characters-in-filename}

In de verouderde app behielden de namen van knooppunten die in de repository zijn gemaakt de ruimten en behuizing van de mapnamen die door de gebruiker zijn verschaft. Als de huidige toepassing de regels voor nodenamen van de v1.10-app moet emuleren, schakelt u [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in de [!UICONTROL Preferences]. Zie [app-voorkeuren](/help/install-upgrade.md#set-preferences). Deze oudere voorkeur is standaard uitgeschakeld.

>[!NOTE]
>
>De app wijzigt alleen de knooppuntnamen in de repository met behulp van de volgende naamconventies. De app behoudt de `Title` van het actief ongewijzigd.

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
| `. / : [ ] | *` | Ingeschakeld of Uitgeschakeld | Vervangen door `-` (afbreekstreepje). A `.` (punt) in de bestandsnaamextensie behouden blijft. | Vervangen door `-` (afbreekstreepje). | `myimage.jpg` ongewijzigd blijft en `my.image.jpg` wijzigingen in `my-image.jpg`. |
| `% ; # , + ? ^ { } "` en witruimte | ![pictogram deselecteren](assets/do-not-localize/deselect-icon.png) Uitgeschakeld | Werkruimten blijven behouden | Vervangen door `-` (afbreekstreepje). | `My Folder.` wijzigingen in `my-folder-`. |
| `# % { } ? & .` | ![pictogram deselecteren](assets/do-not-localize/deselect-icon.png) Uitgeschakeld | Vervangen door `-` (afbreekstreepje). | NA. | `#My New File.` wijzigingen in `-My New File-`. |
| Hoofdletters | ![pictogram deselecteren](assets/do-not-localize/deselect-icon.png) Uitgeschakeld | Trappen blijft ongewijzigd. | Veranderd in kleine letters. | `My New Folder` wijzigingen in `my-new-folder`. |
| Hoofdletters | ![geselecteerd pictogram](assets/do-not-localize/selection-checked-icon.png) Ingeschakeld | Trappen blijft ongewijzigd. | Trappen blijft ongewijzigd. | NA. |

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

![Op de werkbalk onderaan ziet u de acties die relevant zijn voor de geselecteerde elementen](assets/actions_bottom_toolbar1_da2.png "De werkbalk onder in het venster toont algemene acties voor de geselecteerde elementen")

![Geen acties op de werkbalk als er geen algemene acties voor de selectie zijn](assets/actions_bottom_toolbar2_da2.png "Geen acties op de werkbalk als er geen algemene acties voor de selectie zijn")

Welke acties beschikbaar zijn op de werkbalk onderaan, is afhankelijk van de status van de geselecteerde bestanden. Als u bijvoorbeeld alleen **[!UICONTROL Edited Locally]** bestanden, ziet u **[!UICONTROL Upload Changes]** pictogram. Als u een combinatie van **[!UICONTROL Edited locally]** en **[!UICONTROL Cloud only]** de **[!UICONTROL Upload Changes]** actie is niet beschikbaar.

### Alle bewerkte afbeeldingen zoeken {#find-all-edited-images}

De toepassing biedt een weergave met de naam **[!UICONTROL Edited locally]**, zodat u snel toegang hebt tot alle bestanden die u lokaal hebt gedownload (via [!UICONTROL Open] of [!UICONTROL Edit] acties) en vervolgens gewijzigd. Met de app kunt u alle lokaal bewerkte elementen selecteren en de wijzigingen met een paar klikken uploaden. In deze weergave worden ook de lokaal bewerkte elementen weergegeven die een bewerkingsconflict hebben.

![Filteren om alle lokaal bewerkte elementen weer te geven](assets/edited_locally_filter_da2.png "Filter om alle lokaal bewerkte elementen weer te geven, bijvoorbeeld voor het bulkuploaden van bewerkingen")

### Bulkupload-elementen {#bulk-upload-assets}

Gebruikers of organisaties, zoals fotografen of creatieve bureaus, kunnen in scenario&#39;s een groot aantal lokale elementen maken, zoals foto&#39;s, retoucheren of selectie uit een grotere set die buiten [!DNL Experience Manager]. Ze kunnen deze grote lokale mappen uploaden naar [!DNL Assets] rechtstreeks vanuit de bureaubladtoepassing. De maphiërarchieën blijven behouden en alle geneste submappen en opgenomen elementen worden geüpload. De geüploade elementen zijn direct ook beschikbaar voor andere gebruikers van dezelfde server. Elementen worden op de achtergrond geüpload, dus de bewerking is niet gekoppeld aan een webbrowsersessie.

![Bulk uploadt meerdere lokale mappen vanaf uw bureaublad naar [!DNL Experience Manager]](assets/upload_local_folders_da2.png "Met Bulk kunt u meerdere lokale mappen vanaf uw bureaublad uploaden naar Experience Manager")

Als na het uploaden de verwachte wijzigingen niet in de app worden weergegeven, klikt u op het pictogram Vernieuwen ![Pictogram Vernieuwen](assets/do-not-localize/refresh.png).

>[!NOTE]
>
>Gebruik geen uploadfunctionaliteit om elementen over twee te migreren [!DNL Experience Manager] implementaties. Zie in plaats daarvan de [migratiegids](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/assets-migration-guide.html).

### Lijst van overgedragen elementen {#list-of-transferred-assets}

Als u de lijst met elementen wilt weergeven die in een bepaalde sessie zijn overgedragen, raadpleegt u [Elementen uploaden naar [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem).

## Geavanceerde workflow: beginnen vanaf de [!DNL Assets] webinterface {#adv-workflow-start-from-aem-ui}

Start zo nodig uw workflow via de webinterface Middelen. De bureaubladtoepassing kan worden geïntegreerd met de [!DNL Experience Manager] om op verzoek over te nemen met behulp van desktophandelingen.

Een bijzonder geval van het beginnen van werkschema van de Webinterface is middelenontdekking. De gebruikersinterface van de Omnissearch bar in Assets biedt een rijke en geavanceerde zoekervaring. U wilt mogelijk eerst naar het gewenste middel zoeken op het web en vervolgens de workflow in de app starten, met [!UICONTROL Desktop Actions]. Sommige voorbeeldgevallen zijn het filteren van zoekresultaten met gebruik van facetten, het zoeken naar een specifiek middel waarvoor een licentie is verleend door Adobe Stock of een aanpassing die door uw organisatie is geïmplementeerd waardoor u een betere detectie kunt uitvoeren via de webinterface.

De functionaliteit van de bureaubladtoepassing wordt gebruikt wanneer u de volgende handelingen uitvoert in de webinterface Middelen:

* De [!UICONTROL Desktop Actions] dat [!UICONTROL Open], [!UICONTROL Edit], en [!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] of [!UICONTROL check-in]

De acties in de webinterface die beschikbaar zijn voor een middel dat in de app is uitgecheckt, zijn bijvoorbeeld [!UICONTROL Open], [!UICONTROL Reveal], en [!UICONTROL Check-in].

![Bureaubladhandelingen in de [!DNL Experience Manager] webinterface](assets/assets_web_actions_da2.png "Bureaubladhandelingen in de webinterface van Experience Manager")

>[!NOTE]
>
>Mogelijk wordt u door de browser gevraagd het starten van [!DNL Adobe Experience Manager] Desktop. Als u wilt genieten van een ononderbroken overdracht van de browser naar de app, schakelt u het desbetreffende selectievakje in zodat de app altijd overneemt.

U kunt de volgende informatie of workflow niet vinden met de webinterface. Gebruik de bureaubladtoepassing omdat de webinterface lokale wijzigingen niet bijhoudt en zich niet bewust is van het volgende:

* Bestanden die lokaal zijn bewerkt.
* Bestanden met een bewerkingsconflict en een manier om dit op te lossen.
* Lokale wijzigingen uploaden naar [!DNL Experience Manager].
* Verschillende statussen van de lokaal beschikbare bestanden.

Integendeel, u kunt het element in de webinterface openen vanaf de bureaubladtoepassing met behulp van de **[!UICONTROL Open In Web]** handeling.

## Geavanceerde workflow: samenwerken aan dezelfde bestanden en bewerkingsconflicten voorkomen {#adv-workflow-collaborate-avoid-conflicts}

In samenwerkingsomgevingen kunnen meerdere gebruikers werken aan dezelfde set elementen die tot versieconflicten kunnen leiden. Volg de volgende aanbevolen procedures om conflicten te voorkomen:

* U kunt geen elementen bewerken door op [!UICONTROL Open]. Bewerk de lokaal gedownloade elementen niet door deze te openen vanuit de bestandssysteemmap. Andere gebruikers weten niet dat het element wordt bewerkt.
* Als u een element wilt bewerken, klikt u altijd op [!UICONTROL Edit]. Het element wordt geopend in de oorspronkelijke toepassing en er wordt een vergrendelingspictogram toegevoegd aan het element, zodat de andere gebruikers weten dat het element wordt bewerkt.
* Klikken [!UICONTROL Toggle Check-in] als u per ongeluk begint met bewerken zonder te klikken [!UICONTROL Edit]. Hiermee voegt u een vergrendelingspictogram toe aan het element. Zelfs als u een element later wilt bewerken, maar wilt voorkomen dat anderen het bewerken, klikt u op [!UICONTROL Toggle Check-in] om het element te vergrendelen.
* Voordat u een element bewerkt, moet u ervoor zorgen dat andere gebruikers het element niet bewerken. Zoek het slotpictogram op de activa.
* Na het voltooien van de bewerkingen uploadt u alle wijzigingen en checkt u het element in.

![Status van het bewerken van conflicten](assets/edits_conflicts_status_da2.png "Status van het bewerken van conflicten")

Als een lokaal gedownload element wordt bijgewerkt op het tabblad [!DNL Experience Manager] server, geeft de app een **[!UICONTROL Modified remotely]** status. U kunt uw lokale kopie verwijderen of uw lokale kopie vernieuwen door op [!UICONTROL Remove] of [!UICONTROL Update] respectievelijk. Via koppelingen in het dialoogvenster kunt u beide versies van het element weergeven.

![Opties om het conflict op te lossen wanneer het element op afstand wordt gewijzigd](assets/modified_remotely_dialog_da2.png "Opties om het conflict op te lossen wanneer het element op afstand wordt gewijzigd")

Als een middel dat u lokaal bewerkt ook zonder uw medeweten op de server wordt bijgewerkt, wordt een **[!UICONTROL Editing Conflict]** status. U kunt één set van de wijzigingen behouden. De updates blijven behouden (klik op **[!UICONTROL Keep Mine]**) en verwijder de bewerking van de andere gebruiker of respecteer de updates van de andere gebruiker en verwijder uw versie (**[!UICONTROL Overwrite Mine]**).

![Opties om een bewerkingsconflict op te lossen](assets/editing_conflict_dialog_da2.png "Opties om een bewerkingsconflict op te lossen")

## Geavanceerde workflow: elementen plaatsen en koppelen in InDesign-bestand {#adv-workflow-place-assets-indesign}

Wanneer u [!DNL Experience Manager] bureaubladtoepassing om bestanden met gekoppelde elementen te openen, worden de middelen vooraf gedownload en in de oorspronkelijke toepassingen geplaatst. Deze workflow werkt alleen als uw oorspronkelijke toepassing ondersteuning biedt voor het plaatsen van koppelingen naar lokale elementen en [!DNL Experience Manager] moet het oplossen van deze verbindingen in de binaire dossiers aan server-zijverwijzingen steunen.

[!DNL Experience Manager] De bureaubladtoepassing ondersteunt deze workflow met een aantal geselecteerde Adobe Creative Cloud-bureaubladtoepassingen en -bestandsindelingen: Adobe InDesign, Adobe Illustrator en Adobe Photoshop. Met de workflow kunt u efficiënt werken met de ondersteunde Creative Cloud-bestanden. Dus als gebruiker A een paar elementen in een InDesign-bestand plaatst en het controleert [!DNL Experience Manager], ziet gebruiker B de elementen in het InDesign-bestand, ook al maken de elementen geen deel uit van het bestand. De middelen worden plaatselijk gedownload op de machine van gebruiker B.

>[!NOTE]
>
>De bureaubladtoepassing kan worden toegewezen aan elk station in Windows. Wijzig de standaardstationsletter echter niet voor vloeiende bewerkingen. Als gebruikers van dezelfde organisatie verschillende stationsletters gebruiken, kunnen ze de elementen die door anderen zijn geplaatst, niet zien. De geplaatste elementen worden niet opgehaald wanneer het pad verandert. De geplaatste elementen blijven in het binaire bestand (bijvoorbeeld INDD) staan en worden niet verwijderd.

Als u de beperkingen van deze workflow wilt weten, raadpleegt u de [systeemvereisten en ondersteunde versies](release-notes.md).

Voer de volgende stappen uit om deze workflow te testen met een afbeeldingselement en InDesign:

1. Houd een INDD-bestand bij de hand met geplaatste elementen in [!DNL Experience Manager]. Ga voor meer informatie over het maken van een dergelijk INDD-bestand naar [Afbeeldingen plaatsen](https://helpx.adobe.com/indesign/using/placing-graphics.html).
1. Vanuit de bureaubladtoepassing **[!UICONTROL Edit]** het INDD-bestand met geplaatste elementen in [!DNL Experience Manager].
1. De app downloadt zowel het InDesign-bestand als de gekoppelde elementen. Wanneer InDesign het document opent, worden de koppelingen opgelost, worden de elementen gedownload en worden de elementen weergegeven in het InDesign-document.
1. Als u een nieuwe afbeelding in het InDesign-bestand wilt plaatsen, gebruikt u **[!UICONTROL Reveal File]** handeling op het actief. De actie downloadt plaatselijk activa en opent de lokale plaats van het netwerkaandeel in de Ontdekkingsreiziger van Vensters of de Vinder van Mac.
1. Plaats het onthulde element in het InDesign-document. Hiermee maakt u een koppeling in het document.
1. Nadat u de bewerkingen in het InDesign-document hebt voltooid, slaat u het document op en uploadt u het naar [!DNL Experience Manager] met de bureaubladtoepassing.

## Geavanceerde workflow: de elementen lokaal downloaden {#adv-workflow-download-assets-locally}

De app downloadt de middelen van [!DNL Experience Manager] in veel gevallen lokaal op uw bestandssysteem te gebruiken. De downloads verbruiken bandbreedte en schijfruimte. Als u de scenario&#39;s kent, kunt u de wachttijd tot de downloads zijn voltooid, optimaliseren.

U kunt de middelen downloaden vanuit de app op aanvraag. Zie [Elementen downloaden](#download-assets).

Wanneer u de [!UICONTROL Open] om middelen te openen in een native desktoptoepassing, wordt het middel lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [Elementen openen](#openondesktop-v2).

Wanneer u de locatie van een middel of een map vanuit de app weergeeft, wordt het middel of de map eerst lokaal gedownload en vervolgens op uw computer geopend in het gedeelde lokale netwerk. Zie [Elementen openen](#openondesktop-v2).

Wanneer u de [!UICONTROL Edit] om middelen in een native desktoptoepassing te bewerken, wordt het middel lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [Elementen bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager]](#edit-assets-upload-updated-assets).

Als de app is geïnstalleerd en u mag deze gebruiken, worden de acties voltooid wanneer u [!UICONTROL Desktop Actions] van [!DNL Experience Manager] webinterface. De app downloadt het middel eerst en voltooit de actie.
