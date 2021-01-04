---
title: ' [!DNL Experience Manager] desktop app versie 1.x installeren en configureren'
description: Installeer en configureer  [!DNL Experience Manager] desktop app version 1.x to work with [!DNL Assets] servers en wijs de middelen toe om als aandrijving op uw Desktop te monteren.
translation-type: tm+mt
source-git-commit: a25c1fa13895ae9eb7268e3e01c83a5f0b9d7d1d
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 0%

---


# [!DNL Experience Manager] desktop app v1.x {#install-and-configure-aem-desktop-app} installeren en configureren

Met de [!DNL Experience Manager]-bureaubladtoepassing zijn de middelen in [!DNL Experience Manager] gemakkelijk toegankelijk op uw lokale bureaublad en kunnen deze worden gebruikt in alle bureaubladtoepassingen. Middelen kunnen eenvoudig worden weergegeven in Mac Finder of Windows Verkenner, worden geopend in bureaubladtoepassingen en lokaal worden gewijzigd. De wijzigingen worden weer opgeslagen in [!DNL Experience Manager] wanneer u uploadt en er wordt een nieuwe versie gemaakt in de opslagplaats.

Een dergelijke integratie maakt het mogelijk dat verschillende functies in de organisatie de bedrijfsmiddelen centraal beheren en deze in de Creative Cloud en andere toepassingen benaderen, terwijl het eenvoudig wordt om de verschillende standaarden, waaronder branding, na te leven.

Als u [!DNL Experience Manager]-bureaubladtoepassing wilt gebruiken,

* Zorg ervoor dat uw [!DNL Experience Manager] serverversie door [!DNL Experience Manager] Desktop app wordt gesteund. Zie [compatibiliteitsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Download en installeer de toepassing.

* Test de verbinding met behulp van een paar elementen. Zie [Elementen openen en openen op uw bureaublad](use-app-v1.md#openondesktop).

## Systeemvereisten, vereisten en downloadkoppelingen {#system-requirements-prerequisites-and-download-links}

Zie de [[!DNL Experience Manager] Opmerkingen bij de release van de bureaubladtoepassing](release-notes-of-v1.md) voor gedetailleerde informatie.

## De toepassing installeren en aansluiten op [!DNL Experience Manager]-server{#install-and-connect-aem-desktop-app-to-aem-server}

Zie [Installeren en verbinden [!DNL Experience Manager] desktop app to [!DNL Experience Manager] server](use-app-v1.md#installandconnect) voor meer informatie.

>[!NOTE]
>
>Er kan slechts één exemplaar van de [!DNL Experience Manager]-bureaubladtoepassing worden geïnstalleerd en tegelijk actief zijn.

## Bestandsverwerking {#file-handling}

Wanneer u een bestand wijzigt van een netwerklocatie die is gekoppeld door de bureaubladtoepassing, worden de bestanden in twee fasen op die locatie opgeslagen. In de eerste fase wordt een bestand lokaal opgeslagen. Een gebruiker kan het bestand opslaan en aan het bestand blijven werken, zonder te wachten tot de overdracht is voltooid.

In de tweede fase uploadt de bureaubladtoepassing het bijgewerkte bestand na een vooraf gedefinieerde vertraging naar de [!DNL Experience Manager]-server (bijvoorbeeld dertig). Deze bewerking vindt plaats op de achtergrond. Met de optie Asset Status weergeven kunt u de status van de uploadbewerking weergeven.

1. Een element uploaden naar elementen.

1. Klik op het pictogram van de [!DNL Experience Manager]-bureaubladtoepassing op de werkbalk.

1. Selecteer in het menu de optie Asset Status weergeven.

1. Controleer in het dialoogvenster de status van de uploadbewerking.

>[!NOTE]
>
>[!DNL Experience Manager] bureaubladtoepassingen kunnen bestanden tot maximaal 40 GB verwerken.

## Verbind met een [!DNL Experience Manager] instantie achter een verzender {#connect-to-an-aem-instance-behind-a-dispatcher}

Voor de kopieer- en verplaatsingsmethoden in de Elementen-API moeten de volgende extra headers worden doorgegeven aan [!DNL Experience Manager]:

* X-bestemming
* X-diepte
* X-Overschrijven

[!DNL Experience Manager] -desktop maakt verbinding  [!DNL Experience Manager] met een URL die de standaardpoort bevat. Daarom zou `virtualhosts` het plaatsen in de configuratie van de verzender het standaardhavenaantal moeten omvatten. Voor meer informatie rond `virtualhosts` configuratie, zie [virtuele gastheren identificeren](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#identifying-virtual-hosts-virtualhosts).

Voor extra informatie bij het vormen van de verzender om door deze extra kopballen over te gaan, zie [het Specificeren van de Kopballen van HTTP](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxyondersteuning {#proxy-support}

[!DNL Experience Manager] desktop-app gebruikt de vooraf gedefinieerde proxy van het systeem om via HTTPS verbinding te maken met internet. De toepassing kan alleen verbinding maken met een netwerkproxy waarvoor geen extra verificatie is vereist.

Als u de instellingen van de proxyserver voor Windows configureert of wijzigt (Internetopties > LAN-instellingen), start u de [!DNL Experience Manager]-bureaubladtoepassing opnieuw om de wijzigingen van kracht te laten worden.

>[!NOTE]
>
>Proxyconfiguratie wordt alleen toegepast wanneer u de bureaubladtoepassing start. Sluit de app en start de app opnieuw om de wijzigingen door te voeren.

Als uw proxy verificatie vereist, kan het IT-team toestaan dat de Experience Manager Assets URL in de instellingen van de proxyserver het toepassingsverkeer doorgeeft.

## Het dialoogvenster Elementinfo aanpassen {#customize-the-asset-info-dialog}

U kunt het dialoogvenster Elementinfo aanpassen door een van deze componenten of beide te bedekken:

* De Granite-gebruikersinterfacepagina op `/libs/dam/gui/content/assets/moreinfo`.

* De HTL `/css/javascript`-component op `/libs/dam/gui/components/admin/moreinfo`.

Welke component wordt bedekt, hangt van de aard van de aanpassing af. Als u wilt wijzigen welke componenten worden weergegeven als onderdeel van het dialoogvenster Asset Info, bedekt u de pagina voor de gebruikersinterface van Granite. Als u de HTML-, CSS- of JavaScript-inhoud van het dialoogvenster wilt wijzigen, bedekt u de HTML-component.

## Cache {#manage-cache} beheren

In Windows bevindt de cache zich op `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, waar een gecodeerde versie van de [!DNL Experience Manager]-host is geconfigureerd in de bureaubladtoepassing. `http://localhost:4502` wordt bijvoorbeeld weergegeven als `http%3A%2F%2Flocalhost%3A4502%2F`.

In Mac OS X bevindt zich een vergelijkbare map op `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### In-app optie om cache {#in-app-option-to-manage-cache} te beheren

U kunt bepalen hoeveel schijfruimte beschikbaar is voor lokale caching-doeleinden. De artefacten van de middelenserver worden lokaal in het cachegeheugen opgeslagen voor een vloeiender ervaring. U kunt de standaardinstellingen aanpassen aan uw wensen. Bovendien kunt u de cache wissen om alle elementen opnieuw op te halen. Als u de gewenste opties wilt instellen, klikt u op het pictogram van de toepassing en klikt u op **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**. ****

>[!NOTE]
>
>Als u de cache wist, blijven de niet-opgeslagen wijzigingen behouden. Elementen die niet op de [!DNL Experience Manager]-server zijn ingeschakeld, blijven behouden en worden niet verwijderd.

### Locatie van cache wijzigen in Windows {#change-location-of-cache-on-windows}

De standaardlocatie van de cache voor de [!DNL Experience Manager]-bureaubladtoepassing is als volgt:

* In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* In Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

`EncodedAEMEndpoint` is het gevormde  [!DNL Experience Manager] eindpunt URL van app. De waarde is een gecodeerde versie van de doel-URL van de [!DNL Experience Manager]-server. Als de toepassing bijvoorbeeld `http://localhost:4502` als doel heeft, is de mapnaam `http%3A%2F%2Flocalhost%3A4502`. Het pad van Windows naar de cachemap in dit voorbeeld is `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Als u de toepassing wilt laten verwijzen naar een andere map of een ander station, bewerkt u het configuratiebestand van de toepassing.

1. Navigeer naar de installatiemap van de app. De standaardlocatie in Windows is `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bewerk het bestand Adobe Experience Manager Desktop.exe.config met een teksteditor.

   Beheerdersrechten zijn vereist om wijzigingen in dit bestand op te slaan.

1. Zoek naar het koord &quot;ProxyCacheRoot&quot;. U ziet dat de waarde ervan is ingesteld op de cachelocatie `%LocalAppData%\Adobe\AssetsCompanion\Cache`. Wijzig deze waarde in een geldig pad.

   >[!NOTE]
   >
   >De app maakt automatisch een *&lt;Encoded AEM Endpoint>* subdirectory. Dit gedrag kan niet worden geconfigureerd.

>[!MORELIKETHIS]
* [Introductie  [!DNL Experience Manager] tot bureaubladtoepassing](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app.html).
* [Desktop- [!DNL Experience Manager] app](use-app-v1.md) gebruiken.
* [Desktop-app [!DNL Experience Manager]  ](troubleshoot-app-v1.md)problemen oplossen.

