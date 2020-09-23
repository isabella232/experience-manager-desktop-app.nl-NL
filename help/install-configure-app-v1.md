---
title: Installeer en configureer AEM bureaubladtoepassing versie 1.x
description: Installeer en configureer AEM bureaubladtoepassing versie 1.x om met AEM Assets-servers te werken en wijs de middelen toe die als een station op uw bureaublad moeten worden gemonteerd.
uuid: 79bc9de9-5708-41f9-ac43-68c1fd2a2129
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.5/ASSETS, SG_EXPERIENCEMANAGER/6.4/ASSETS,SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: f6365302-1690-4719-9b8c-035719422740
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6a8a49865d2707f5d60fbd6d5e99b597c333d3d5
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---


# Installeer en configureer AEM desktop app v1.x {#install-and-configure-aem-desktop-app}

Met de AEM desktop-app zijn de middelen in AEM gemakkelijk toegankelijk op uw lokale bureaublad en kunnen deze worden gebruikt in alle bureaubladtoepassingen. Elementen kunnen eenvoudig worden weergegeven in Mac Finder of Windows Verkenner, worden geopend in bureaubladtoepassingen en lokaal worden gewijzigd. De wijzigingen worden weer opgeslagen in AEM wanneer u uploadt en er wordt een nieuwe versie gemaakt in de opslagplaats.

Een dergelijke integratie maakt het mogelijk dat verschillende rollen in de organisatie de bedrijfsmiddelen centraal in AEM Assets beheren en ze in de Creative Cloud en andere toepassingen benaderen, terwijl het eenvoudig wordt om de verschillende normen, waaronder branding, na te leven.

Ga als volgt te werk om AEM bureaubladtoepassing te gebruiken:

* Zorg ervoor dat uw AEM serverversie wordt ondersteund door AEM bureaubladtoepassing. Zie de [compatibiliteitsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Download en installeer de toepassing.

* Test de verbinding met behulp van een paar elementen. Zie [Toegang tot middelen en open elementen op uw bureaublad](use-app-v1.md#openondesktop).

## Systeemvereisten, vereisten en downloadkoppelingen {#system-requirements-prerequisites-and-download-links}

Zie de opmerkingen bij de release [AEM desktop app voor meer informatie](release-notes-of-v1.md).

## Installeer en verbind AEM bureaubladtoepassing met AEM server {#install-and-connect-aem-desktop-app-to-aem-server}

Zie [Installeer en verbind AEM bureaubladtoepassing met AEM server](use-app-v1.md#installandconnect)voor meer informatie.

>[!NOTE]
>
>Er kan slechts één exemplaar van de AEM-bureaubladtoepassing worden geïnstalleerd en tegelijkertijd actief zijn.

## Bestandsverwerking {#file-handling}

Wanneer u een bestand wijzigt van een netwerklocatie die is gekoppeld door de bureaubladtoepassing, worden de bestanden in twee fasen op die locatie opgeslagen. In de eerste fase wordt een bestand lokaal opgeslagen. Een gebruiker kan het bestand opslaan en aan het bestand blijven werken, zonder te wachten tot de overdracht is voltooid.

In de tweede fase uploadt de bureaubladtoepassing het bijgewerkte bestand na een vooraf gedefinieerde vertraging naar AEM server (bijvoorbeeld dertig). Deze bewerking vindt plaats op de achtergrond. Met de optie Asset Status weergeven kunt u de status van de uploadbewerking weergeven.

1. Middelen uploaden naar AEM Assets.

1. Klik of tik op het pictogram van de AEM-bureaubladtoepassing op de werkbalk.

1. Selecteer in het menu de optie Asset Status weergeven.

1. Controleer in het dialoogvenster de status van de uploadbewerking.

>[!NOTE]
>
>AEM bureaubladtoepassing kan maximaal 40 GB aan middelen verwerken.

## Verbinding maken met een AEM-instantie achter een dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Voor de kopieer- en verplaatsingsmethoden in de API voor middelen moeten de volgende aanvullende koppen worden doorgegeven aan AEM:

* X-bestemming
* X-diepte
* X-Overschrijven

AEM desktop maakt verbinding met AEM via een URL die de standaardpoort bevat. Daarom zou het plaatsen in de `virtualhosts` dispatcherconfiguratie het standaardhavenaantal moeten omvatten. Voor meer informatie over `virtualhosts` configuratie, zie virtuele gastheren [](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#identifying-virtual-hosts-virtualhosts)identificeren.

Voor extra informatie bij het vormen van de verzender om door deze extra kopballen over te gaan, zie het [Specificeren van de Kopballen](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#specifying-the-http-headers-to-pass-through-clientheaders)van HTTP.

### Proxyondersteuning {#proxy-support}

AEM bureaubladtoepassing gebruikt de vooraf gedefinieerde proxy van het systeem om via HTTPS verbinding te maken met internet. De toepassing kan alleen verbinding maken met een netwerkproxy waarvoor geen extra verificatie is vereist.

Als u de instellingen van de proxyserver voor Windows configureert of wijzigt (Internet-opties > LAN-instellingen), start u de AEM bureaubladtoepassing opnieuw om de wijzigingen van kracht te laten worden.

>[!NOTE]
>
>Proxyconfiguratie wordt alleen toegepast wanneer u de bureaubladtoepassing start. Sluit de app en start de app opnieuw om de wijzigingen door te voeren.

Als uw proxy verificatie vereist, kan het IT-team toestaan dat de Experience Manager Assets URL in de instellingen van de proxyserver het toepassingsverkeer doorgeeft.

## Het dialoogvenster Elementinfo aanpassen {#customize-the-asset-info-dialog}

U kunt het dialoogvenster Elementinfo aanpassen door een van deze componenten of beide te bedekken:

* De Granite-gebruikersinterfacepagina bij `/libs/dam/gui/content/assets/moreinfo`.

* De HTML- `/css/javascript` component op `/libs/dam/gui/components/admin/moreinfo`.

Welke component wordt bedekt, hangt van de aard van de aanpassing af. Als u wilt wijzigen welke componenten worden weergegeven als onderdeel van het dialoogvenster Asset Info, bedekt u de pagina voor de gebruikersinterface van Granite. Als u de HTML-, CSS- of JavaScript-inhoud van het dialoogvenster wilt wijzigen, bedekt u de HTML-component.

## Cache beheren {#manage-cache}

In Windows bevindt de cache zich op `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, waar een gecodeerde versie van de AEM host is geconfigureerd in de bureaubladtoepassing. Bijvoorbeeld, `http://localhost:4502` verschijnt als `http%3A%2F%2Flocalhost%3A4502%2F`.

In Mac OS X bevindt zich een vergelijkbare map `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### Optie voor in-app beheren van cache {#in-app-option-to-manage-cache}

U kunt bepalen hoeveel schijfruimte beschikbaar is voor lokale caching-doeleinden. De artefacten van de AEM Assets-server worden lokaal in het cachegeheugen opgeslagen voor een vloeiender ervaring. U kunt de standaardinstellingen aanpassen aan uw wensen. Bovendien kunt u de cache wissen om alle elementen opnieuw op te halen. Als u de gewenste opties wilt instellen, klikt u op het pictogram van de toepassing en klikt u op **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**. ****

>[!NOTE]
>
>Als u de cache wist, blijven de niet-opgeslagen wijzigingen behouden. Elementen die niet in AEM server zijn ingecheckt, blijven behouden en worden niet verwijderd.

### Locatie van cache in Windows wijzigen {#change-location-of-cache-on-windows}

De standaardlocatie van de cache voor de AEM desktop-app is als volgt:

* In Windows `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* In Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

`EncodedAEMEndpoint` is de geconfigureerde AEM-URL van AEM bureaubladtoepassing. De waarde is een gecodeerde versie van het doel-URL van de AEM server. Als de toepassing zich bijvoorbeeld richt op `http://localhost:4502`de toepassing, is de mapnaam `http%3A%2F%2Flocalhost%3A4502`. Het Windows-pad naar de cachemap in dit voorbeeld is %LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502.

Als u de toepassing wilt laten verwijzen naar een andere map of een ander station, bewerkt u het configuratiebestand van de toepassing.

1. Navigeer naar de installatiemap van de app. De standaardlocatie in Windows is `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bewerk het bestand Adobe Experience Manager Desktop.exe.config met een teksteditor.

   Beheerdersrechten zijn vereist om wijzigingen in dit bestand op te slaan.

1. Zoek naar het koord &quot;ProxyCacheRoot&quot;. U ziet dat de waarde is ingesteld op de cachelocatie &quot;%LocalAppData%\Adobe\AssetsCompanion\Cache&quot;. Wijzig deze waarde in een geldig pad.

   >[!NOTE]
   >
   >De toepassing maakt automatisch een submap *&lt;Encoded AEM Endpoint>* . Dit gedrag kan niet worden geconfigureerd.

>[!MORELIKETHIS]
* [Inleiding tot AEM bureaubladtoepassing](https://helpx.adobe.com/customer-care-office-hours/aem/desktop-app.html)
* [AEM bureaubladtoepassing gebruiken](use-app-v1.md)
* [Inchecken/uitchecken begrijpen met AEM bureaubladtoepassing](https://docs.adobe.com/content/help/en/experience-manager-learn/assets/collaboration/checkin-checkout-technical-video-understand.html)
* [Desktop-app gebruiken met AEM Assets](https://docs.adobe.com/content/help/en/experience-manager-learn/assets/collaboration/checkin-checkout-technical-video-understand.html)
* [Problemen met AEM bureaubladtoepassing oplossen](troubleshoot-app-v1.md)

