---
title: Aanbevolen werkwijzen voor en probleemoplossing voor Adobe Experience Manager-bureaubladtoepassingen
description: Volg de beste praktijken en los problemen op om de af en toe met installatie, verbetering, configuratie, etc. verband houdende kwesties op te lossen.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.5/ASSETS, SG_EXPERIENCEMANAGER/6.4/ASSETS, SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 381e586077c7db63dd57a468b1c6abc60c63e34e
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 0%

---


# Problemen met Adobe Experience Manager-bureaubladtoepassing oplossen {#troubleshoot-v2}

Adobe Experience Manager (AEM) desktop app maakt verbinding met de DAM-opslagplaats (Digital Asset Management) van een externe Experience Manager. De app haalt opslaggegevens en zoekresultaten op uw computer op, downloadt en uploadt bestanden en mappen en bevat mogelijkheden om conflicten met de gebruikersinterface van AEM Assets te beheren.

Lees verder om de app problemen op te lossen, de beste werkwijzen te leren en de beperkingen uit te zoeken.

## Best practices {#best-practices-to-prevent-troubles}

Houd u aan de volgende aanbevolen procedures om bepaalde algemene problemen en problemen te voorkomen.

* **Begrijp hoe de desktop-app werkt**: Voordat u de toepassing gaat gebruiken, moet u even weten hoe de app werkt. U weet hoe u een koppeling tot stand brengt tussen de webinterface van de Experience Manager en het bureaublad, de toewijzing van opslagruimten, het in cache plaatsen van elementen, het lokaal opslaan en het uploaden op de achtergrond. Zie [hoe het werkt](release-notes.md#how-app-works).

* **Gebruik geen niet-ondersteunde tekens in mapnamen**: Gebruik geen spaties en ongeldige tekens bij het maken of uploaden van mappen. Zie een lijst met tekens bij [Mappen maken in Experience Manager Assets](https://docs.adobe.com/content/help/en/experience-manager-65/assets/managing/managing-assets-touch-ui.html#Creatingfolders). Sommige Adobe Experience Manager-gebruiksgevallen kunnen worden beïnvloed door niet-ondersteunde tekens in de mapnaam.

* **Tips en trucs om conflicten** te voorkomen: Zie [Bewerkingsconflicten](using.md#adv-workflow-collaborate-avoid-conflicts)voorkomen om potentiële conflicten te voorkomen wanneer u samenwerkt met meerdere elementen.

* **Mapupload gebruiken voor grote, hiërarchische mappen**: Gebruik in plaats van de webinterface Middelen of andere methoden de bureaubladtoepassing Experience Manager om grote mappen te uploaden. De app uploadt de middelen op de achtergrond met registratie en controle. Zie [bulkuploadmiddelen](using.md#bulk-upload-assets).

* **Gebruik de nieuwste versie**: Gebruik de nieuwste versie van de app en controleer altijd op compatibiliteit voordat u een nieuwe app-versie installeert of voordat u een upgrade uitvoert naar een nieuwere Adobe Experience Manager-versie. Zie [opmerkingen bij](release-notes.md)de release.

* **Dezelfde stationsletter** gebruiken: Gebruik dezelfde stationsletter in een organisatie om toe te wijzen aan de Adobe Experience Manager DAM. Als u elementen wilt zien die door andere gebruikers zijn geplaatst, moeten de paden gelijk zijn. Als u dezelfde stationsletter gebruikt, hebt u een constant pad naar DAM-middelen. De elementen blijven geplaatst en worden niet verwijderd, zelfs niet als verschillende stationsletters door verschillende gebruikers worden gebruikt.

* **Denk aan het netwerk**: Netwerkprestaties zijn essentieel voor de prestaties van de desktop-app van de Experience Manager. Als u te maken krijgt met een trage reactie op bestandsoverdrachten of bulkbewerkingen, schakelt u de functies of toepassingen uit die veel netwerkverkeer kunnen veroorzaken.

* **Niet-ondersteunde gebruiksgevallen voor bureaubladtoepassing**: Gebruik de app voor de migratie van middelen niet (hiervoor zijn planning en andere hulpmiddelen nodig); voor zware DAM-bewerkingen (zoals het verplaatsen van grote mappen, grote uploads, het zoeken van bestanden met behulp van geavanceerde metagegevenszoekopdrachten); en als synchronisatieclient (ontwerpprincipes en gebruikspatronen verschillen van in-sync clients zoals Microsoft OneDrive of Adobe Creative Cloud-desktopsynchronisatie).

* **Time-out**: Desktop-app heeft momenteel geen configureerbare time-outwaarde die de verbinding tussen Experience Manager-server en desktop-app na een vast tijdsinterval verbreekt. Wanneer u grote middelen uploadt en de verbinding na een tijdje wordt verbroken, probeert de toepassing het element een paar keer te uploaden door de time-out van het uploaden te verhogen. Er is geen aanbevolen manier om de standaardtime-outinstellingen te wijzigen.

## Hoe te om problemen op te lossen {#troubleshooting-prep}

Houd rekening met de volgende informatie als u problemen met bureaubladtoepassingen wilt oplossen. Bovendien is het programma klaar om de problemen beter door te geven aan de klantenservice van Adobe als u ervoor kiest om ondersteuning te zoeken.

### Foutopsporingsmodus inschakelen {#enable-debug-mode}

Als u problemen wilt oplossen, kunt u de foutopsporingsmodus inschakelen en meer informatie in de logboeken opnemen.

>[!NOTE]
>
>Geldige logboekniveaus zijn DEBUG, INFO, WARN, of FOUT. De breedste logboeken zijn het hoogst in DEBUG en het laagste in FOUT.

Zo gebruikt u de toepassing in de foutopsporingsmodus op de Mac:

1. Open een eindvenster of een bevelherinnering.

1. Start de [!DNL Experience Manager] bureaubladtoepassing met de volgende opdracht:

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

De foutopsporingsmodus in Windows inschakelen:

1. Open een opdrachtvenster.

1. Start de [!DNL Experience Manager] bureaubladtoepassing met de volgende opdracht:

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### Locatie van logbestanden {#check-log-files-v2}

[!DNL Experience Manager] de logbestanden van de bureaubladtoepassing worden op de volgende locaties opgeslagen, afhankelijk van het besturingssysteem:

In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Op Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

Als bij het uploaden van een groot aantal bestanden sommige bestanden niet worden geüpload, raadpleegt u het bestand om de mislukte uploads te identificeren. `backend.log`

>[!NOTE]
>
>Wanneer u met de klantenservice van Adobe werkt aan een supportverzoek of -ticket, kunt u worden gevraagd de logbestanden te delen om het zorgteam van de klant te helpen het probleem te begrijpen. Archiveer de volledige `Logs` map en deel deze met uw contactpersoon voor de klantenservice.

### Cache wissen {#clear-cache-v2}

Het wissen AEM de cache van de bureaublad-app is een voorlopige taak voor het oplossen van problemen die verschillende problemen kan oplossen. Wis de cache uit de toepassingsvoorkeuren. Zie [Voorkeuren](install-upgrade.md#set-preferences)instellen. De standaardlocatie van de cachemap is:

* In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

* Op Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

Nochtans, kan de plaats afhankelijk van het gevormde AEM eindpunt van AEM Desktop veranderen. De waarde is een gecodeerde versie van de beoogde URL. Als de toepassing zich bijvoorbeeld richt op `http://localhost:4502`de toepassing, is de mapnaam `http%3A%2F%2Flocalhost%3A4502%2F`. Als u de cache wilt wissen, verwijdert u de desbetreffende map. Een andere reden om cache te wissen is het vrijmaken van schijfruimte wanneer er weinig schijfruimte beschikbaar is.

>[!CAUTION]
>
>Als u AEM bureaubladcache wist, gaan wijzigingen in lokale elementen die niet op AEM server worden gesynchroniseerd, onherroepelijk verloren.

### De versie van de AEM bureaubladtoepassing kennen {#know-app-version-v2}

Klik op het menu ![](assets/do-not-localize/more_options_da2.png) App om het menu van de app te openen en klik op **[!UICONTROL Help]** > **[!UICONTROL About]**.

## Kan geplaatste elementen niet zien {#placed-assets-missing}

Controleer het volgende als u niet kunt zien welke elementen u of andere creatieve professionals in de ondersteuningsbestanden hebben geplaatst (bijvoorbeeld INDD-bestanden):

* Verbinding maken met de server. De Flash-netwerkconnectiviteit kan het downloaden van bedrijfsmiddelen blokkeren.
* Bestandsgrootte. Het downloaden en weergeven van grote elementen duurt langer.
* Stationsconsistentie. Als u of een andere medewerker de elementen heeft geplaatst terwijl de AEM DAM is toegewezen aan een andere stationsletter, worden de geplaatste elementen niet weergegeven.
* Machtigingen. Neem contact op met de AEM om te controleren of u machtigingen hebt om de geplaatste elementen op te halen.

## Problemen bij upgraden op MacOS {#issues-when-upgrading-on-macos}

Soms kunnen er problemen optreden wanneer u een upgrade uitvoert van AEM bureaubladtoepassing op MacOS. Dit wordt veroorzaakt door de oude systeemmap van AEM bureaubladtoepassing, waardoor nieuwe versies van AEM bureaubladtoepassing niet correct kunnen worden geladen. U kunt dit probleem verhelpen door de volgende mappen en bestanden handmatig te verwijderen.

Sleep de `Adobe Experience Manager Desktop` toepassing van de map MacOS Applications naar de prullenmand voordat u de volgende stappen uitvoert. Open vervolgens de terminal, voer de volgende opdracht uit en geef uw wachtwoord op wanneer u daarom wordt gevraagd.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Kan bestanden niet uploaden {#upload-fails}

Als u bureaubladtoepassingen gebruikt met AEM 6.5.1 of hoger, moet u de S3- of Azure-aansluiting upgraden naar versie 1.10.4 of hoger. Het probleem met de fout bij het uploaden van bestanden met betrekking tot [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599)is opgelost. Zie [installatie-instructies](install-upgrade.md#install-v2).

## [!DNL Experience Manager] verbindingsproblemen met bureaubladapps {#connection-issues}

### SAML-aanmeldverificatie werkt niet {#da-connection-issue-with-saml-aem}

Als de [!DNL Experience Manager] bureaubladtoepassing geen verbinding maakt met uw [!DNL Adobe Experience Manager] instantie SSO-enabled (SAML), leest u deze sectie voor het oplossen van problemen. SSO-processen zijn gevarieerd, soms complex, en het ontwerp van de toepassing doet zijn best om deze typen verbindingen aan te passen. Nochtans, vereisen sommige montages extra het oplossen van problemen.

Soms wordt het SAML-proces niet omgeleid naar het oorspronkelijk gevraagde pad of is de uiteindelijke omleiding naar een host die anders is dan wat in de [!DNL Adobe Experience Manager] bureaubladtoepassing is geconfigureerd. Om na te gaan of dit niet het geval is:

1. Open een webbrowser.

1. Voer de URL `<AEM host>/content/dam.json` in op de adresbalk.

   Vervangen `<AEM host>` door bijvoorbeeld de [!DNL Adobe Experience Manager] doelinstantie `http://localhost:4502/content/dam.json`.

1. Meld u aan bij de [!DNL Adobe Experience Manager] instantie.

1. Wanneer login volledig is, bekijk het huidige adres van browser in de adresbar. Deze moet exact overeenkomen met de URL die oorspronkelijk is ingevoerd.

1. Controleer ook of alles voordat het bestand `/content/dam.json` overeenkomt met de [!DNL Adobe Experience Manager] doelwaarde die in de instellingen van de [!DNL Adobe Experience Manager] bureaubladtoepassing is geconfigureerd.

**Het SAML-aanmeldingsproces werkt correct volgens de bovenstaande stappen, maar gebruikers kunnen zich nog steeds niet aanmelden**

Het venster binnen de [!DNL Adobe Experience Manager] bureaubladtoepassing waarin het aanmeldingsproces wordt weergegeven, is gewoon een webbrowser die de webgebruikersinterface van de [!DNL Adobe Experience Manager] doelinstantie weergeeft:

* De versie van MAC gebruikt een [WebView](https://developer.apple.com/documentation/webkit/webview).

* In de Windows-versie wordt op chroom gebaseerde [CefSharp](https://cefsharp.github.io/)gebruikt.

Zorg ervoor dat het SAML-proces deze browsers ondersteunt.

Als u meer problemen wilt oplossen, kunt u de exacte URL&#39;s bekijken die de browser probeert te laden. Deze informatie bekijken:

1. Volg de aanwijzingen voor het starten van de toepassing in de [foutopsporingsmodus](#enable-debug-mode).

1. Reproduceer de login poging.

1. Ga naar de [logmap](#check-log-files-v2) van de toepassing

1. Voor Windows:

   1. Open &quot;aemcompanionlog.txt&quot;.

   1. Zoek naar berichten die met &quot;Login browser adres veranderen in&quot;beginnen. Deze vermeldingen bevatten ook de URL die de toepassing heeft geladen.

   Voor Mac:

   1. `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`, waarbij de **n** wordt vervangen door de nummers in de nieuwste bestandsnaam.

   1. Zoek naar berichten die met &quot;geladen kader&quot;beginnen. Deze vermeldingen bevatten ook de URL die de toepassing heeft geladen.


Het bekijken van de opeenvolging URL die wordt geladen kan helpen bij het eind van SAML problemen oplossen om te bepalen wat verkeerd is.

### Probleem met SSL-configuratie {#ssl-config-v2}

De bibliotheken die AEM bureaubladtoepassing gebruikt voor HTTP-communicatie maken gebruik van strikte SSL-afgedwongen omzetting. Soms kan een verbinding met een browser slagen, maar wordt AEM bureaubladtoepassing niet gebruikt. Installeer het ontbrekende tussentijdse certificaat in Apache om SSL op de juiste wijze te configureren. Zie [Een tussenpersoon installeren in Apache](https://access.redhat.com/solutions/43575).

## App reageert niet {#unresponsive}

In zeldzame gevallen reageert de toepassing niet meer, wordt alleen een wit scherm weergegeven of wordt een fout onder aan de interface weergegeven zonder opties in de interface. Probeer het volgende in de volgorde:

* Klik met de rechtermuisknop op de toepassingsinterface en klik op **[!UICONTROL Refresh]**.
* Sluit de toepassing af en open deze opnieuw.

In beide methoden wordt de toepassing gestart in de hoofdmap DAM.

>[!MORELIKETHIS]
>
>* [Bekende problemen](release-notes.md#known-issues-v2)
>* [Bewerkingsconflicten voorkomen](using.md#adv-workflow-collaborate-avoid-conflicts)

