---
title: Desktop-app v1.10 installeren en configureren
description: Installeren en configureren [!DNL Experience Manager] bureaubladtoepassing versie 1.10 om te werken met [!DNL Assets] -servers en de middelen toewijzen die als een station op uw bureaublad moeten worden gemonteerd.
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 78f18e68178f711d925d7e308822c657087d009a
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Installeren en configureren [!DNL Experience Manager] desktop app v1.10 {#install-and-configure-aem-desktop-app}

Met de [!DNL Experience Manager] bureaubladtoepassing, de middelen binnen [!DNL Experience Manager] zijn gemakkelijk toegankelijk op uw lokale bureaublad en kunnen in om het even welke Desktoptoepassingen worden gebruikt. Elementen kunnen eenvoudig worden weergegeven in Mac Finder of Windows Verkenner, worden geopend in bureaubladtoepassingen en lokaal worden gewijzigd. De wijzigingen worden opgeslagen in [!DNL Experience Manager] wanneer u uploadt en er een nieuwe versie wordt gemaakt in de repository.

Een dergelijke integratie maakt het mogelijk dat verschillende functies in de organisatie de bedrijfsmiddelen centraal beheren en deze in de Creative Cloud en andere toepassingen benaderen, terwijl het eenvoudig wordt om zich aan de verschillende normen te houden, waaronder branding.

Te gebruiken [!DNL Experience Manager] bureaubladtoepassing,

* Zorg ervoor dat uw [!DNL Experience Manager] serverversie wordt ondersteund door [!DNL Experience Manager] bureaubladtoepassing. Zie de [compatibiliteitsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Download en installeer de toepassing.

* Test de verbinding met behulp van een paar elementen. Zie [Elementen openen en openen op uw bureaublad](use-app-v1.md#openondesktop).

## Systeemvereisten, vereisten en downloadkoppelingen {#system-requirements-prerequisites-and-download-links}

Zie voor meer informatie de [[!DNL Experience Manager] Opmerkingen bij de release bureaubladapp](release-notes-of-v1.md).

## De toepassing installeren en verbinden met [!DNL Experience Manager] server {#install-and-connect-aem-desktop-app-to-aem-server}

Zie voor meer informatie [Installeren en verbinden [!DNL Experience Manager] bureaubladtoepassing naar [!DNL Experience Manager] server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Slechts één instantie van de [!DNL Experience Manager] bureaubladtoepassing kan worden geïnstalleerd en tegelijk actief zijn.

## Bestandsverwerking {#file-handling}

Wanneer u een bestand wijzigt van een netwerklocatie die is gekoppeld door de bureaubladtoepassing, worden de bestanden in twee fasen op die locatie opgeslagen. In de eerste fase wordt een bestand lokaal opgeslagen. Een gebruiker kan het bestand opslaan en aan het bestand blijven werken, zonder te wachten tot de overdracht is voltooid.

In de tweede fase wordt het bijgewerkte bestand geüpload naar [!DNL Experience Manager] server na een vooraf gedefinieerde vertraging (bijvoorbeeld 30 seconden). Deze bewerking vindt plaats op de achtergrond. Met de optie Asset Status weergeven kunt u de status van de uploadbewerking weergeven.

1. Een element uploaden naar elementen.

1. Klik op de knop [!DNL Experience Manager] bureaubladtoepassing vanuit de werkbalk.

1. Selecteer in het menu de optie Asset Status weergeven.

1. Controleer in het dialoogvenster de status van de uploadbewerking.

>[!NOTE]
>
>[!DNL Experience Manager] bureaubladtoepassingen kunnen bestanden tot maximaal 40 GB verwerken.

## Verbinding maken met een [!DNL Experience Manager] instantie achter een verzender {#connect-to-an-aem-instance-behind-a-dispatcher}

Voor de kopieer- en verplaatsingsmethoden in de API voor middelen moeten de volgende aanvullende koppen worden doorgegeven aan [!DNL Experience Manager]:

* X-bestemming
* X-diepte
* X-Overschrijven

[!DNL Experience Manager] desktop maakt verbinding met [!DNL Experience Manager] via een URL die de standaardpoort bevat. Daarom `virtualhosts` het plaatsen in de dispatcherconfiguratie zou het standaardhavenaantal moeten omvatten. Voor meer informatie over `virtualhosts` configuratie, zie [virtuele hosts identificeren](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#identifying-virtual-hosts-virtualhosts).

Voor extra informatie bij het vormen van de verzender om door deze extra kopballen over te gaan, zie [De HTTP-headers opgeven](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxyondersteuning {#proxy-support}

[!DNL Experience Manager] desktop-app gebruikt de vooraf gedefinieerde proxy van het systeem om via HTTPS verbinding te maken met internet. De toepassing kan alleen verbinding maken met een netwerkproxy waarvoor geen extra verificatie is vereist.

Als u de instellingen van de proxyserver voor Windows configureert of wijzigt (Internet Options > LAN Settings), start u de [!DNL Experience Manager] bureaubladtoepassing voor de wijzigingen die van kracht worden.

>[!NOTE]
>
>Proxyconfiguratie wordt alleen toegepast wanneer u de bureaubladtoepassing start. Sluit de app en start de app opnieuw om de wijzigingen door te voeren.

Als uw proxy verificatie vereist, kan het IT-team de Experience Manager Assets URL in de instellingen van de proxyserver toestaan om het toepassingsverkeer door te geven.

## Het dialoogvenster Elementinfo aanpassen {#customize-the-asset-info-dialog}

U kunt het dialoogvenster Elementinfo aanpassen door een van deze componenten of beide te bedekken:

* De gebruikersinterfacepagina van Granite op `/libs/dam/gui/content/assets/moreinfo`.

* De HTML `/css/javascript` component bij `/libs/dam/gui/components/admin/moreinfo`.

Welke component wordt bedekt, hangt van de aard van de aanpassing af. Als u wilt wijzigen welke componenten worden weergegeven als onderdeel van het dialoogvenster Asset Info, bedekt u de pagina voor de gebruikersinterface van Granite. Bedek de HTML-component om de HTML-, CSS- of JavaScript-inhoud van het dialoogvenster te wijzigen.

## Cache beheren {#manage-cache}

In Windows bevindt de cache zich op `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, waarbij een gecodeerde versie van de [!DNL Experience Manager] host geconfigureerd in de bureaubladtoepassing. Bijvoorbeeld: `http://localhost:4502` verschijnt zoals `http%3A%2F%2Flocalhost%3A4502%2F`.

In Mac OS X staat een vergelijkbare map op `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### Optie voor in-app beheren van cache {#in-app-option-to-manage-cache}

U kunt bepalen hoeveel schijfruimte beschikbaar is voor lokale caching-doeleinden. De artefacten van de middelenserver worden lokaal in het cachegeheugen opgeslagen voor een vloeiender ervaring. U kunt de standaardinstellingen aanpassen aan uw wensen. Bovendien kunt u de cache wissen om alle elementen opnieuw op te halen. Als u de gewenste opties wilt instellen, klikt u op het pictogram van de toepassing en klikt u op **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**. ****

>[!NOTE]
>
>Als u de cache wist, blijven de niet-opgeslagen wijzigingen behouden. Elementen die niet zijn geselecteerd in [!DNL Experience Manager] server worden behouden en niet verwijderd.

### Locatie van cache in Windows wijzigen {#change-location-of-cache-on-windows}

De standaardlocatie van de cache voor de [!DNL Experience Manager] desktop app is als volgt:

* In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* In Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

`EncodedAEMEndpoint` is geconfigureerd voor toepassing [!DNL Experience Manager] eindpunt-URL. De waarde is een gecodeerde versie van de URL voor het opgeven van doelen voor het [!DNL Experience Manager] server. Als de toepassing zich bijvoorbeeld richt op `http://localhost:4502`, is de mapnaam `http%3A%2F%2Flocalhost%3A4502`. Het pad van Windows naar de cachemap in dit voorbeeld is `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Als u de toepassing wilt laten verwijzen naar een andere map of een ander station, bewerkt u het configuratiebestand van de toepassing.

1. Navigeer naar de installatiemap van de app. De standaardlocatie in Windows is `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bewerk het bestand Adobe Experience Manager Desktop.exe.config met een teksteditor.

   Beheerdersrechten zijn vereist om wijzigingen in dit bestand op te slaan.

1. Zoek naar het koord &quot;ProxyCacheRoot&quot;. U ziet dat de waarde ervan is ingesteld op de cachelocatie `%LocalAppData%\Adobe\AssetsCompanion\Cache`. Wijzig deze waarde in een geldig pad.

   >[!NOTE]
   >
   >De app maakt automatisch een *&lt;encoded aem=&quot;&quot; endpoint=&quot;&quot;>* subdirectory. Dit gedrag kan niet worden geconfigureerd.

>[!MORELIKETHIS]
* [Inleiding tot [!DNL Experience Manager] bureaubladtoepassing](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app.html).
* [Gebruiken [!DNL Experience Manager] bureaubladtoepassing](use-app-v1.md).
* [Problemen oplossen [!DNL Experience Manager] bureaubladtoepassing](troubleshoot-app-v1.md).

