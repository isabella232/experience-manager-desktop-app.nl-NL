---
title: Aanbevolen werkwijzen voor en probleemoplossing voor de Adobe Experience Manager-bureaubladtoepassing
description: Follow best practices and troubleshoot to resolve the occasional issues related to installation, upgrade, configuration, and so on.
uuid: ce98a3e7-5454-41be-aaaa-4252b3e0f8dd
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f5eb222a-6cdf-4ae3-9cf2-755c873f397c
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ac4be2cb69a112f393ec76d5d95987634d0c9c46

---


# Troubleshoot Adobe Experience Manager desktop app {#troubleshoot-v2}

De bureaubladtoepassing Adobe Experience Manager (AEM) maakt verbinding met de DAM-opslagplaats (Digital Asset Management) van een externe Experience Manager. De app haalt opslaggegevens en zoekresultaten op uw computer op, downloadt en uploadt bestanden en mappen en bevat mogelijkheden voor het beheren van conflicten met de gebruikersinterface van AEM Assets.

Lees verder om de app problemen op te lossen, de beste werkwijzen te leren en de beperkingen uit te zoeken.

## Aanbevolen procedures {#best-practices-to-prevent-troubles}

Houd u aan de volgende aanbevolen procedures om bepaalde algemene problemen en problemen te voorkomen.

* **Begrijp hoe de desktop-app werkt**: Voordat u de toepassing gaat gebruiken, moet u enkele minuten controleren hoe de app werkt. U weet hoe u een koppeling tot stand brengt tussen de webinterface en het bureaublad, de toewijzing van opslagruimte, het in cache plaatsen van elementen, lokaal opslaan en uploaden op de achtergrond. See [how it works](release-notes.md#how-app-works).

* **Avoid unsupported characters in folder names**: Do not use white spaces and invalid characters when creating or uploading folders. Zie een lijst met tekens in [Mappen maken in Experience Manager-elementen](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html#Creatingfolders). Bepaalde Adobe Experience Manager-gebruiksgevallen kunnen worden beïnvloed door niet-ondersteunde tekens in de mapnaam.

* **Best practices to avoid conflicts**: To avoid potential conflicts when collaborating on multiple assets, see [avoid editing conflicts](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Use folder upload for large, hierarchical folders**: Instead of using the Assets web interface or other methods, use Experience Manager desktop app to upload large folders. The app uploads the assets in background with logging and monitoring. See [bulk upload assets](using.md#bulk-upload-assets).

* **Use the latest version**: Use the latest app version and always check for compatibility before installing either a new app version or before upgrading to a newer Adobe Experience Manager version. See [release notes](release-notes.md).

* **Use the same drive letter**: Use the same drive letter across an organization to map to the Adobe Experience Manager DAM. To see assets placed by other users, the paths must be the same. Using the same drive letter ensures a constant path to DAM assets. De elementen blijven geplaatst en worden niet verwijderd, zelfs niet als verschillende stationsletters door verschillende gebruikers worden gebruikt.

* **Denk aan het netwerk**: Netwerkprestaties zijn van essentieel belang voor de prestaties van de Desktop-app van Experience Manager. Als u te maken krijgt met een trage reactie op bestandsoverdrachten of bulkbewerkingen, schakelt u de functies of toepassingen uit die veel netwerkverkeer kunnen veroorzaken.

* **Unsupported use cases for desktop app**: Do not use the app for Assets&#39; migration (it needs planning and other tools); for heavy-duty DAM operations (like moving large folders, large uploads, finding files using advanced metadata searches); and as a sync client (design principles and usage patterns are different from in-sync clients like Microsoft OneDrive or Adobe Creative Cloud desktop sync).

* **Timeout**: Currently, desktop app does not have a configurable timeout value that disconnects the connection between Experience Manager server and desktop app after a fixed time interval. When uploading large assets, if the connection gets timeout after a while, the app retries to upload the asset a few times by increasing the upload timeout. Er is geen aanbevolen manier om de standaardtime-outinstellingen te wijzigen.

## How to troubleshoot {#troubleshooting-prep}

Houd rekening met de volgende informatie als u problemen met bureaubladtoepassingen wilt oplossen. Also, it prepares you to better convey the issues to Adobe Customer Care if you choose to seek support.

### Enable debug mode {#enable-debug-mode}

Als u problemen wilt oplossen, kunt u de foutopsporingsmodus inschakelen en meer informatie in de logboeken opnemen. Als u de toepassing wilt uitvoeren in de foutopsporingsmodus, gebruikt u de volgende opdrachtregelopties in een terminal of bij de opdrachtprompt.

* In Windows: `SET AEM_DESKTOP_LOG_LEVEL=DEBUG & "C:\Program Files\Adobe\Adobe Experience Manager Desktop\Adobe Experience Manager Desktop.exe"`

* Op Mac: `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`

### Locatie van logbestanden {#check-log-files-v2}

You can find the log files for AEM desktop app at the following locations. Als bij het uploaden van een groot aantal bestanden sommige bestanden niet worden geüpload, raadpleegt u het bestand op de bovenstaande locatie om de mislukte uploads te identificeren. `backend.log`

* On Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

* Op Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

>[!NOTE]
>
>When working with Adobe Customer Care on a support request/ticket, you may be asked to share the log files to help the support team understand the issue. Archiveer de volledige `Logs` map en deel deze met de klantenservice.

### Cache wissen {#clear-cache-v2}

Het wissen van het cachegeheugen van de AEM-bureaubladtoepassing is een voorlopige taak voor het oplossen van problemen die verschillende problemen kan oplossen. Wis de cache uit de toepassingsvoorkeuren. Zie [Voorkeuren](install-upgrade.md#set-preferences)instellen. De standaardlocatie van de cachemap is:

* In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

* Op Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

Nochtans, kan de plaats afhankelijk van het gevormde eindpunt van AEM Desktop veranderen AEM. De waarde is een gecodeerde versie van de beoogde URL. Als de toepassing zich bijvoorbeeld richt op `http://localhost:4502`de toepassing, is de mapnaam `http%3A%2F%2Flocalhost%3A4502%2F`. Als u de cache wilt wissen, verwijdert u de desbetreffende map. Een andere reden om cache te wissen is het vrijmaken van schijfruimte wanneer er weinig schijfruimte beschikbaar is.

>[!CAUTION]
>
>Als u de AEM-bureaubladcache wist, gaan wijzigingen in lokale elementen die niet op de AEM-server zijn gesynchroniseerd, onherroepelijk verloren.

### De AEM-bureaubladtoepassingsversie kennen {#know-app-version-v2}

Klik op het menu ![](assets/do-not-localize/more_options_da2.png) App om het menu van de app te openen en klik op **[!UICONTROL Help]** > **[!UICONTROL About]**.

## Kan geplaatste elementen niet zien {#placed-assets-missing}

Controleer het volgende als u niet kunt zien welke elementen u of andere creatieve professionals in de ondersteuningsbestanden hebben geplaatst (bijvoorbeeld INDD-bestanden):

* Verbinding maken met de server. De Flash-netwerkconnectiviteit kan het downloaden van bedrijfsmiddelen blokkeren.
* Bestandsgrootte. Het downloaden en weergeven van grote elementen duurt langer.
* Stationsconsistentie. Als u of een andere medewerker de elementen heeft geplaatst terwijl de AEM DAM is toegewezen aan een andere stationsletter, worden de geplaatste elementen niet weergegeven.
* Machtigingen. Neem contact op met de AEM-beheerder om te controleren of u machtigingen hebt om de geplaatste elementen op te halen.

## Problemen bij upgraden op MacOS {#issues-when-upgrading-on-macos}

Soms kunnen er problemen optreden wanneer u de AEM-bureaubladtoepassing op MacOS upgradet. Dit wordt veroorzaakt door een oudere systeemmap voor de AEM-bureaubladtoepassing, waardoor nieuwe versies van de AEM-bureaubladtoepassing niet correct kunnen worden geladen. U kunt dit probleem verhelpen door de volgende mappen en bestanden handmatig te verwijderen.

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

## Probleem met SSL-configuratie {#ssl-config-v2}

De bibliotheken die AEM-bureaubladtoepassingen gebruiken voor HTTP-communicatie, maken gebruik van strikte SSL-afgedwongen omzetting. Soms kan een verbinding met een browser slagen, maar wordt de AEM-bureaubladtoepassing niet gebruikt. Installeer het ontbrekende tussentijdse certificaat in Apache om SSL op de juiste wijze te configureren. Zie [Een tussenpersoon installeren in Apache](https://access.redhat.com/solutions/43575).

## App reageert niet {#unresponsive}

In zeldzame gevallen reageert de toepassing niet meer, wordt alleen een wit scherm weergegeven of wordt een fout onder aan de interface weergegeven zonder opties in de interface. Probeer het volgende in de volgorde:

1. Klik met de rechtermuisknop op de toepassingsinterface en klik op **[!UICONTROL Refresh]**.
1. Sluit de toepassing af en start deze opnieuw.

In beide methoden wordt de toepassing gestart in de hoofdmap DAM.

>[!MORELIKETHIS]
>
>* [Bekende problemen](release-notes.md#known-issues-v2)
>* [Bewerkingsconflicten voorkomen](using.md#adv-workflow-collaborate-avoid-conflicts)