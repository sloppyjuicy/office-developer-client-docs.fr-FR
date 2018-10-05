---
title: Extension de la barre météorologique dans Outlook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b355b98-dd7d-4f16-8257-367e5dd61b34
description: Découvrez comment ajouter un service web météorologique tiers à la barre météorologique dans Outlook 2013, afin de fournir des données de conditions météorologiques pour un lieu choisi par l'utilisateur.
ms.openlocfilehash: 0423e149306bf7562dd525f1b7460a63cbace372
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386578"
---
# <a name="extending-the-weather-bar-in-outlook"></a><span data-ttu-id="fbf55-103">Extension de la barre météorologique dans Outlook</span><span class="sxs-lookup"><span data-stu-id="fbf55-103">Extending the Weather Bar in Outlook</span></span>

<span data-ttu-id="fbf55-104">Découvrez comment ajouter un service web météorologique tiers à la barre météorologique dans Outlook 2013, afin de fournir des données de conditions météorologiques pour un lieu choisi par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fbf55-104">Learn how to plug in a third-party weather web service for the Weather Bar in Outlook 2013, to provide weather conditions data for a user-chosen location.</span></span>
  
## <a name="weather-bar-overview"></a><span data-ttu-id="fbf55-105">Présentation de la barre météorologique</span><span class="sxs-lookup"><span data-stu-id="fbf55-105">Weather Bar overview</span></span>
<span data-ttu-id="fbf55-106"><a name="ol15_weatherbar_overview"> </a></span><span class="sxs-lookup"><span data-stu-id="fbf55-106"><a name="ol15_weatherbar_overview"> </a></span></span>

<span data-ttu-id="fbf55-p101">La barre météorologique d'Outlook affiche les conditions et prévisions météorologiques relatives à un lieu géographique. Un utilisateur peut choisir un ou plusieurs lieux et consulter facilement les données météorologiques affichées dans la barre météorologique du module de calendrier. La figure 1 présente la barre météorologique affichant une prévision sur trois jours de la météo à New York.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p101">The Weather Bar in Outlook displays weather conditions and forecast for a geographic location. A user can choose one or multiple locations, and conveniently see weather data in the Weather Bar in the calendar module. Figure 1 shows the Weather Bar displaying a three-day forecast for New York, NY.</span></span> 
  
<span data-ttu-id="fbf55-110">**Figure 1. Barre météorologique dans Outlook**</span><span class="sxs-lookup"><span data-stu-id="fbf55-110">**Figure 1. Weather Bar in Outlook**</span></span>

![Barre météo affichant les prévisions pour New York](media/ol15_WeatherBar_fig1.jpg)
  
<span data-ttu-id="fbf55-p102">Les paramètres de la barre météorologique sont enregistrés avec le profil utilisateur. Selon le type de compte Outlook, les paramètres peuvent suivre l'utilisateur vers tous les ordinateurs sur lesquels l'utilisateur ouvre une session à l'aide du même profil, comme c'est le cas pour les comptes Exchange. Sinon, l'utilisateur peut personnaliser ses paramètres sur chaque ordinateur, comme pour les comptes IMAP/POP.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p102">Settings for the Weather Bar are saved with the user's profile. Depending on the type of Outlook account, the settings may roam with the user on all computers that the user logs on to with the same profile, as in the case of Exchange accounts. Alternatively, the user can customize settings on each computer, as in the case of IMAP/POP accounts.</span></span>
  
<span data-ttu-id="fbf55-p103">Par défaut, Outlook utilise les données météorologiques fournies par MSN Météo. La barre météorologique prend en charge les services web de données météorologiques tiers qui suivent un protocole défini pour communiquer avec Outlook. Tant qu'un service de données météorologiques tiers prend en charge ce protocole, les utilisateurs peuvent choisir que ce service de données météorologiques fournisse les données météorologiques de la barre météorologique. Cet article décrit le protocole visant à intégrer les services météorologiques tiers à la barre météorologique Outlook.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p103">By default, Outlook uses weather data provided by MSN Weather. The Weather Bar supports third-party weather data web services that follow a defined protocol to communicate with Outlook. As long as a third-party weather data service supports this protocol, users can choose that weather data service to provide weather data in the Weather Bar. This article describes the protocol for third-party weather services to integrate with Outlook in the Weather Bar.</span></span>
  
## <a name="weather-bar-protocol"></a><span data-ttu-id="fbf55-119">Protocole de la barre météorologique</span><span class="sxs-lookup"><span data-stu-id="fbf55-119">Weather Bar protocol</span></span>
<span data-ttu-id="fbf55-120"><a name="ol15_weatherbar_theprotocol"> </a></span><span class="sxs-lookup"><span data-stu-id="fbf55-120"><a name="ol15_weatherbar_theprotocol"> </a></span></span>

<span data-ttu-id="fbf55-121">Un utilisateur peut indiquer un autre service de données météorologiques pour la barre météorologique, tant que ce service implémente un service web qui prend en charge le protocole suivant pour communiquer avec Outlook :</span><span class="sxs-lookup"><span data-stu-id="fbf55-121">A user can specify a different weather data service for the Weather Bar, as long as that weather data service implements a web service that supports the following protocol to communicate with Outlook:</span></span>
  
1. <span data-ttu-id="fbf55-p104">Le service de données météorologique prend en charge une URL de base d'un service web. Par exemple, un service web Contoso Météo peut avoir une URL de base correspondant à https://service.contoso.com/data.aspx.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p104">The weather data service supports a base URL to a web service. For example, a Contoso Weather web service can have a base URL of https://service.contoso.com/data.aspx.</span></span>
    
2. <span data-ttu-id="fbf55-124">Pour demander un code d’emplacement, le service web autorise Outlook à ajouter les paramètres suivants à l’URL de base :</span><span class="sxs-lookup"><span data-stu-id="fbf55-124">The web service allows Outlook to append the following parameters to the base URL, to request a location code:</span></span> 
    
   - <span data-ttu-id="fbf55-125">outputview=search : ce paramètre indique que la demande est une recherche d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="fbf55-125">outputview=search: This parameter indicates that the request is a location search.</span></span>
    
   - <span data-ttu-id="fbf55-126">weasearchstr=_city_ : ce paramètre indique le lieu (_ville_), pour lequel l'utilisateur souhaite recevoir des prévisions météorologiques (par exemple, Londres).</span><span class="sxs-lookup"><span data-stu-id="fbf55-126">weasearchstr= _city_: This parameter indicates the location,  _city_, for which the user wants a weather forecast (for example, London).</span></span>
    
   - <span data-ttu-id="fbf55-127">culture=_LCID_ : ce paramètre indique la culture de la version d’Office installée pour l’utilisateur sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fbf55-127">culture= _LCID_: This parameter indicates the culture of the version of Office installed for the user on that computer.</span></span> <span data-ttu-id="fbf55-128">La valeur LCID est définie dans les balises [[ RFC4646] qui permettent d’identifier les langues](https://www.ietf.org/rfc/rfc4646.txt)</span><span class="sxs-lookup"><span data-stu-id="fbf55-128">The LCID value is defined in [[RFC4646] Tags for Identifying Languages](https://www.ietf.org/rfc/rfc4646.txt)</span></span>
    
   - <span data-ttu-id="fbf55-129">src=outlook : ce paramètre indique qu’Outlook est l’application cliente demandant le service.</span><span class="sxs-lookup"><span data-stu-id="fbf55-129">src=outlook: This parameter indicates that Outlook is the client application requesting the service.</span></span>
    
   <span data-ttu-id="fbf55-p106">Ces paramètres permettent à Outlook de connaître le lieu qui intéresse l'utilisateur et de rechercher le code d'emplacement associé pris en charge par le service de données météorologiques. Le service web doit répondre à Outlook avec un code d'emplacement sous la forme d'un code XML conforme au [Outlook Weather Location XML Schema](outlook-weather-location-xml-schema.md). La figure 2 récapitule la demande et la réponse du service web relatives à un code d'emplacement.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p106">These parameters allow Outlook to take the location that the user is interested in and search for the associated location code as supported by the weather data service. The web service should respond to Outlook with a location code in XML that follows the [Outlook Weather Location XML Schema](outlook-weather-location-xml-schema.md). Figure 2 summarizes the web service request and response for a location code.</span></span>
    
   <span data-ttu-id="fbf55-133">**Figure 2. Demande de service web et réponse pour un code d'emplacement**</span><span class="sxs-lookup"><span data-stu-id="fbf55-133">**Figure 2. Web service request and response for a location code**</span></span>

   ![Demande météo et réponse en fonction du lieu](media/ol15_WeatherBar_Fig02.gif)
  
3. <span data-ttu-id="fbf55-135">Pour demander un code de lieu, le service web autorise également Outlook à ajouter les paramètres suivants à l’URL de base :</span><span class="sxs-lookup"><span data-stu-id="fbf55-135">The web service also allows Outlook to append the following parameters, to request forecast information for a location code:</span></span>
    
   - <span data-ttu-id="fbf55-136">wealocations=_code_ : « _code_ » dans ce paramètre représente le code de lieu qu'Outlook obtient lors de l’étape 2. Ce code permet d'identifier le lieu qui intéresse l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fbf55-136">wealocations= _code_: _code_ in this parameter is a location code that Outlook obtains from Step 2, and that maps to the location that the user is interested in.</span></span> 
    
   - <span data-ttu-id="fbf55-137">weadegreetype=_degreetype_ : ce paramètre spécifie si vous souhaitez utiliser les unités de mesure métriques ou impériales pour la température.</span><span class="sxs-lookup"><span data-stu-id="fbf55-137">weadegreetype= _degreetype_: This parameter specifies whether to use metric or imperial units of measurement for temperature.</span></span> <span data-ttu-id="fbf55-138">Pour _degreetype_, spécifiez c pour métrique, f pour impérial.</span><span class="sxs-lookup"><span data-stu-id="fbf55-138">Specify c for metric, f for imperial for  _degreetype_.</span></span> <span data-ttu-id="fbf55-139">Ce paramètre est facultatif et n’est pas toujours disponible dans la demande de service web.</span><span class="sxs-lookup"><span data-stu-id="fbf55-139">This parameter is optional and does not always exist in the web service request.</span></span>
    
   - <span data-ttu-id="fbf55-140">culture=_LCID_ : ce paramètre indique la culture de la version d’Office installée pour l’utilisateur sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fbf55-140">culture= _LCID_: This parameter indicates the culture of the version of Office installed for the user on that computer.</span></span> <span data-ttu-id="fbf55-141">La valeur LCID est définie dans les balises [[ RFC4646] qui permettent d’identifier les langues](https://www.ietf.org/rfc/rfc4646.txt)</span><span class="sxs-lookup"><span data-stu-id="fbf55-141">The LCID value is defined in [[RFC4646] Tags for Identifying Languages](https://www.ietf.org/rfc/rfc4646.txt)</span></span>
    
   - <span data-ttu-id="fbf55-142">src=outlook : ce paramètre indique qu’Outlook est l’application cliente demandant le service.</span><span class="sxs-lookup"><span data-stu-id="fbf55-142">src=outlook: This parameter indicates that Outlook is the client application requesting the service.</span></span>
    
   <span data-ttu-id="fbf55-p109">Ces paramètres permettent à Outlook de prendre le code d'emplacement renvoyé à l'étape 2 et de demander des prévisions météorologiques au service de données. Le service web doit répondre à Outlook avec les données météorologiques correspondantes sous la forme d'un code XML conforme au [Outlook Weather Information XML Schema](outlook-weather-information-xml-schema.md). La figure 3 récapitule la demande et la réponse du service web relatives à un code d'emplacement.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p109">These parameters allow Outlook to take the location code returned from Step 2 and request the weather data service for the forecast. The web service should respond to Outlook with the corresponding weather data in XML that follows the [Outlook Weather Information XML Schema](outlook-weather-information-xml-schema.md). Figure 3 summarizes the web service request and response for weather data given a location code.</span></span>
    
   <span data-ttu-id="fbf55-146">**Figure 3. Demande de service web et réponse pour des informations météorologiques**</span><span class="sxs-lookup"><span data-stu-id="fbf55-146">**Figure 3. Web service request and response for weather information**</span></span>

   ![Demande d’infos météo et réponse](media/ol15_WeatherBar_Fig03.gif)
  
## <a name="setting-the-weather-bar-to-use-a-weather-service"></a><span data-ttu-id="fbf55-148">Définition de la barre météorologique afin d'utiliser un service météo</span><span class="sxs-lookup"><span data-stu-id="fbf55-148">Setting the Weather Bar to use a weather service</span></span>
<span data-ttu-id="fbf55-149"><a name="ol15_weatherbar_setting"> </a></span><span class="sxs-lookup"><span data-stu-id="fbf55-149"><a name="ol15_weatherbar_setting"> </a></span></span>

<span data-ttu-id="fbf55-p110">L'administrateur ou l'utilisateur avancé peut utiliser la clé de Registre **WeatherServiceUrl** pour personnaliser la barre météorologique afin d'utiliser un service météo spécifique. Par exemple, si l'URL de base pour un service météo Contoso est https://service.contoso.com/data.aspx, vous pouvez définir la clé **WeatherServiceUrl** sur cette URL.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p110">The administrator or power user can use the **WeatherServiceUrl** registry key to customize the Weather Bar to use a specific weather service. For example, if the base URL for a Contoso weather service is https://service.contoso.com/data.aspx, you can set the **WeatherServiceUrl** key to that URL.</span></span> 
  
<span data-ttu-id="fbf55-152">Le tableau suivant décrit la clé **WeatherServiceUrl**.</span><span class="sxs-lookup"><span data-stu-id="fbf55-152">The following table describes the **WeatherServiceUrl** key.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbf55-153">**Clé**</span><span class="sxs-lookup"><span data-stu-id="fbf55-153">**Key**</span></span> <br/> |<span data-ttu-id="fbf55-154">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span><span class="sxs-lookup"><span data-stu-id="fbf55-154">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span></span>  <br/> |
|<span data-ttu-id="fbf55-155">**Nom de valeur**</span><span class="sxs-lookup"><span data-stu-id="fbf55-155">**Value name**</span></span> <br/> |<span data-ttu-id="fbf55-156">**WeatherServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="fbf55-156">**WeatherServiceUrl**</span></span> <br/> |
|<span data-ttu-id="fbf55-157">**Type de valeur**</span><span class="sxs-lookup"><span data-stu-id="fbf55-157">**Value type**</span></span> <br/> |<span data-ttu-id="fbf55-158">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="fbf55-158">REG_SZ</span></span>  <br/> |
|<span data-ttu-id="fbf55-159">**Valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="fbf55-159">**Default value**</span></span> <br/> |<span data-ttu-id="fbf55-160">EMPTY_STRING</span><span class="sxs-lookup"><span data-stu-id="fbf55-160">EMPTY_STRING</span></span>  <br/> |
|<span data-ttu-id="fbf55-161">**Description**</span><span class="sxs-lookup"><span data-stu-id="fbf55-161">**Description**</span></span> <br/> |<span data-ttu-id="fbf55-162">URL d'un service de données météorologiques.</span><span class="sxs-lookup"><span data-stu-id="fbf55-162">URL to a weather data service.</span></span>  <br/> |
   
## <a name="dependent-conditions"></a><span data-ttu-id="fbf55-163">Conditions dépendantes</span><span class="sxs-lookup"><span data-stu-id="fbf55-163">Dependent conditions</span></span>
<span data-ttu-id="fbf55-164"><a name="ol15_weatherbar_dependentconditions"> </a></span><span class="sxs-lookup"><span data-stu-id="fbf55-164"><a name="ol15_weatherbar_dependentconditions"> </a></span></span>

<span data-ttu-id="fbf55-p111">Outlook 2013 affiche la barre météorologique par défaut. Cette section décrit quelques raisons pour lesquelles la barre météorologique pourrait ne pas être visible.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p111">Outlook 2013 displays the Weather Bar by default. This section describes a few reasons why the Weather Bar might not be visible.</span></span>
  
### <a name="weather-bar-is-disabled"></a><span data-ttu-id="fbf55-167">La barre météorologique est désactivée</span><span class="sxs-lookup"><span data-stu-id="fbf55-167">Weather Bar is disabled</span></span>

<span data-ttu-id="fbf55-168">Tout d'abord, vérifiez que l'option **Afficher la météo sur le calendrier** est sélectionnée dans l'onglet **Calendrier** de la boîte de dialogue **Options Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fbf55-168">First, verify that **Show weather on the calendar** is selected in the **Calendar** tab in the **Outlook Options** dialog box.</span></span> 
  
<span data-ttu-id="fbf55-169">Notez qu'un administrateur peut également utiliser la stratégie de groupe pour complètement désactiver la barre météorologique dans Outlook 2013 en définissant la clé suivante dans le Registre Windows :</span><span class="sxs-lookup"><span data-stu-id="fbf55-169">Note that an administrator can also use Group Policy to disable the Weather Bar in Outlook 2013 entirely by setting the following key in the Windows registry:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbf55-170">**Clé**</span><span class="sxs-lookup"><span data-stu-id="fbf55-170">**Key**</span></span> <br/> |<span data-ttu-id="fbf55-171">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span><span class="sxs-lookup"><span data-stu-id="fbf55-171">HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar</span></span>  <br/> |
|<span data-ttu-id="fbf55-172">**Nom de valeur**</span><span class="sxs-lookup"><span data-stu-id="fbf55-172">**Value name**</span></span> <br/> |<span data-ttu-id="fbf55-173">**DisableWeather**</span><span class="sxs-lookup"><span data-stu-id="fbf55-173">**DisableWeather**</span></span> <br/> |
|<span data-ttu-id="fbf55-174">**Type de valeur**</span><span class="sxs-lookup"><span data-stu-id="fbf55-174">**Value type**</span></span> <br/> |<span data-ttu-id="fbf55-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="fbf55-175">REG_DWORD</span></span>  <br/> |
|<span data-ttu-id="fbf55-176">**Valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="fbf55-176">**Default value**</span></span> <br/> |<span data-ttu-id="fbf55-177">0</span><span class="sxs-lookup"><span data-stu-id="fbf55-177">0</span></span>  <br/> |
|<span data-ttu-id="fbf55-178">**Description**</span><span class="sxs-lookup"><span data-stu-id="fbf55-178">**Description**</span></span> <br/> |<span data-ttu-id="fbf55-179">Une valeur de 0 active la barre météorologique. Toute autre valeur la désactive.</span><span class="sxs-lookup"><span data-stu-id="fbf55-179">A value of 0 enables the Weather Bar; any other value disables the Weather Bar.</span></span>  <br/> |
   
<span data-ttu-id="fbf55-p112">Si la fonctionnalité de barre météorologique a été désactivée par la stratégie de groupe, l'onglet **Calendrier** ne comprend pas la case à cocher **Afficher la météo sur le calendrier**. Consultez l'administrateur pour réactiver la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p112">If the Weather Bar feature has been disabled by Group Policy, the **Calendar** tab does not include the **Show weather on the calendar** check box. Consult with the administrator to turn the feature back on.</span></span> 
  
### <a name="office-is-disconnected-from-the-internet"></a><span data-ttu-id="fbf55-182">Office est déconnecté d'Internet</span><span class="sxs-lookup"><span data-stu-id="fbf55-182">Office is disconnected from the Internet</span></span>

<span data-ttu-id="fbf55-183">Vérifiez qu'Office est en mesure de se connecter à Internet. Pour ce faire, accédez à l'onglet **Options de confidentialité** du **Centre de gestion de la confidentialité** en mode Backstage et assurez-vous que l'option **Autoriser Office à se connecter à Internet** est activée.</span><span class="sxs-lookup"><span data-stu-id="fbf55-183">Verify that Office is enabled to connect to the Internet—go to the **Privacy options** tab of the **Trust Center** in the Backstage view, and ensure that **Allow Office to connect to the Internet** is selected.</span></span> 
  
<span data-ttu-id="fbf55-184">Si l'utilisateur a choisi de ne pas recevoir les mises à jour pour Office, la barre météorologique est également désactivée.</span><span class="sxs-lookup"><span data-stu-id="fbf55-184">If the user has chosen to not receive updates for Office, the Weather Bar is also disabled.</span></span>
  
<span data-ttu-id="fbf55-185">Un administrateur peut également utiliser la stratégie de groupe pour désactiver tous les contenus en ligne, y compris la barre météorologique, en définissant la clé suivante dans le Registre Windows :</span><span class="sxs-lookup"><span data-stu-id="fbf55-185">An administrator can also use Group Policy to disable all online content, including the Weather Bar, by setting the following key in the Windows registry:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbf55-186">**Clé**</span><span class="sxs-lookup"><span data-stu-id="fbf55-186">**Key**</span></span> <br/> |<span data-ttu-id="fbf55-187">HKCU\Software\Microsoft\Office\15.0\Common\Internet</span><span class="sxs-lookup"><span data-stu-id="fbf55-187">HKCU\Software\Microsoft\Office\15.0\Common\Internet</span></span>  <br/> |
|<span data-ttu-id="fbf55-188">**Nom de valeur**</span><span class="sxs-lookup"><span data-stu-id="fbf55-188">**Value name**</span></span> <br/> |<span data-ttu-id="fbf55-189">**UseOnlineContent**</span><span class="sxs-lookup"><span data-stu-id="fbf55-189">**UseOnlineContent**</span></span> <br/> |
|<span data-ttu-id="fbf55-190">**Type de valeur**</span><span class="sxs-lookup"><span data-stu-id="fbf55-190">**Value type**</span></span> <br/> |<span data-ttu-id="fbf55-191">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="fbf55-191">REG_DWORD</span></span>  <br/> |
|<span data-ttu-id="fbf55-192">**Valeur par défaut**</span><span class="sxs-lookup"><span data-stu-id="fbf55-192">**Default value**</span></span> <br/> |<span data-ttu-id="fbf55-193">2</span><span class="sxs-lookup"><span data-stu-id="fbf55-193">2</span></span>  <br/> |
|<span data-ttu-id="fbf55-194">**Description**</span><span class="sxs-lookup"><span data-stu-id="fbf55-194">**Description**</span></span> <br/> |<span data-ttu-id="fbf55-195">Une valeur de 2 active la barre météorologique. Toute autre valeur la désactive.</span><span class="sxs-lookup"><span data-stu-id="fbf55-195">A value of 2 enables the Weather Bar; any other value disables the Weather Bar.</span></span>  <br/> |
   
<span data-ttu-id="fbf55-p113">Si la fonctionnalité de barre météorologique a été désactivée par la stratégie de groupe, l'onglet **Calendrier** ne comprend pas la case à cocher **Afficher la météo sur le calendrier**. Consultez l'administrateur pour réactiver la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p113">If the Weather Bar feature has been disabled by Group Policy, the **Calendar** tab does not include the **Show weather on the calendar** check box. Consult with the administrator to turn the feature back on.</span></span> 
  
## <a name="weather-bar-example"></a><span data-ttu-id="fbf55-198">Exemple de barre météorologique</span><span class="sxs-lookup"><span data-stu-id="fbf55-198">Weather Bar example</span></span>
<span data-ttu-id="fbf55-199"><a name="ol15_weatherbar_example"> </a></span><span class="sxs-lookup"><span data-stu-id="fbf55-199"><a name="ol15_weatherbar_example"> </a></span></span>

<span data-ttu-id="fbf55-p114">Cette section présente un exemple d'un service météo Contoso qui suit le protocole mentionné précédemment pour communiquer avec Outlook. Pour tout emplacement que l'utilisateur sélectionne, Outlook obtient d'abord un code d'emplacement de la part de Contoso Météo, puis ce code est utilisé pour appeler le service Contoso Météo afin d'obtenir les données météorologiques.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p114">This section shows an example of a Contoso Weather service that follows the preceding protocol to communicate with Outlook. For any location that the user selects, Outlook first gets a location code for that location from Contoso Weather, then using that location code, calls the Contoso Weather service to get the weather data.</span></span>
  
### <a name="base-url"></a><span data-ttu-id="fbf55-202">URL de base</span><span class="sxs-lookup"><span data-stu-id="fbf55-202">Base URL</span></span>

<span data-ttu-id="fbf55-203">Contoso Météo fournit l'URL de base suivante pour leur service de données météorologiques :</span><span class="sxs-lookup"><span data-stu-id="fbf55-203">Contoso Weather provides the following base URL for their weather data service:</span></span>
  
https://service.contoso.com/data.aspx
  
### <a name="getting-a-location-code"></a><span data-ttu-id="fbf55-204">Obtention d'un code d'emplacement</span><span class="sxs-lookup"><span data-stu-id="fbf55-204">Getting a location code</span></span>

<span data-ttu-id="fbf55-205">Outlook ajoute les paramètres décrits lors de l'étape 2 à l'URL de base afin d'obtenir le code d'emplacement d'un lieu géographique ( _city_) :</span><span class="sxs-lookup"><span data-stu-id="fbf55-205">Outlook appends the parameters described in Step 2 above to the base URL to obtain the location code for a geographic location  _city_:</span></span>
  
<span data-ttu-id="fbf55-206">https://service.contoso.com/data.aspx?outputview=search&amp;weasearchstr= _city_</span><span class="sxs-lookup"><span data-stu-id="fbf55-206">https://service.contoso.com/data.aspx?outputview=search&amp;weasearchstr= _city_</span></span>
  
<span data-ttu-id="fbf55-207">À titre d'exemple, si l'utilisateur a sélectionné Tokyo dans la barre météorologique, Outlook utilise l'URL suivante pour obtenir le code d'emplacement de Tokyo auprès de Contoso Météo :</span><span class="sxs-lookup"><span data-stu-id="fbf55-207">As an example, if the user has selected Tokyo in the Weather Bar, Outlook uses the following URL to obtain the location code for Tokyo from Contoso Weather:</span></span> 
  
<span data-ttu-id="fbf55-208">https://weather.service.contoso.com/data.aspx?outputview=search&amp;weasearchstr=tokyo</span><span class="sxs-lookup"><span data-stu-id="fbf55-208">https://weather.service.contoso.com/data.aspx?outputview=search&amp;weasearchstr=tokyo</span></span>
  
<span data-ttu-id="fbf55-p115">Contoso Météo répond avec le code XML suivant pour fournir le code d'emplacement de Tokyo. Le code XML est conforme au schéma XML d'emplacement météorologique d'Outlook. Notez que les services météorologiques renvoient souvent des données correspondant à plus d'un emplacement (par exemple, si l'emplacement choisi est une grande zone métropolitaine). Dans cet exemple, la réponse pour Tokyo comprend deux emplacements, chacun compris dans un élément [weather](weather-element-weatherdata-elementoutlook-weather-location-schema.md). Les codes d'emplacement correspondants sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fbf55-p115">Contoso Weather responds with the following XML to provide the location code for Tokyo. The XML conforms to the Outlook Weather Location XML Schema. Note that it is common for weather services to return data for more than one location (for example, if the selected location is a greater metropolitan area). In this example, the response for Tokyo includes two locations, each enclosed in a [weather](weather-element-weatherdata-elementoutlook-weather-location-schema.md) element. The corresponding location codes are as follows:</span></span> 
  
- <span data-ttu-id="fbf55-214">wc:JAXX0085 si l'attribut **weatherlocationname** est  `Tokyo, JPN`</span><span class="sxs-lookup"><span data-stu-id="fbf55-214">wc:JAXX0085 for the **weatherlocationname** attribute being  `Tokyo, JPN`</span></span>
    
- <span data-ttu-id="fbf55-215">wc:10038604 si l'attribut **weatherlocationname** est  `Shinjuku-ku, Tokyo, Japan`</span><span class="sxs-lookup"><span data-stu-id="fbf55-215">wc:10038604 for the **weatherlocationname** attribute being  `Shinjuku-ku, Tokyo, Japan`</span></span>
    
```XML
<?xml version="1.0" ?>
<weatherdata>
  <weather weatherlocationcode="wc:JAXX0085" 
    weatherlocationname="Tokyo, JPN">
  </weather>
  <weather weatherlocationcode="wc:10038604" 
    weatherlocationname="Shinjuku-ku, JPN">
  </weather>
</weatherdata>

```

### <a name="getting-weather-information-for-a-location-code"></a><span data-ttu-id="fbf55-216">Obtention d'informations météorologiques pour un code d'emplacement</span><span class="sxs-lookup"><span data-stu-id="fbf55-216">Getting weather information for a location code</span></span>

<span data-ttu-id="fbf55-217">Après avoir obtenu le code d'emplacement pour un lieu donné, Outlook ajoute les paramètres décrits lors de l'étape 3 à l'URL de base afin d'obtenir des informations météorologiques relatives au code d'emplacement.</span><span class="sxs-lookup"><span data-stu-id="fbf55-217">After obtaining the location code for a location, Outlook appends the parameters described in Step 3 above to the base URL to obtain weather information for that location code.</span></span>
  
<span data-ttu-id="fbf55-218">https://service.contoso.com/data.aspx?wealocations= _code_</span><span class="sxs-lookup"><span data-stu-id="fbf55-218">https://service.contoso.com/data.aspx?wealocations= _code_</span></span>
  
<span data-ttu-id="fbf55-219">À titre d'exemple, si Outlook a obtenu le code d'emplacement wc:JAXX0085 auprès de Contoso Météo pour Tokyo, Outlook utilise ce code d'emplacement dans l'URL suivante pour obtenir les informations météorologiques.</span><span class="sxs-lookup"><span data-stu-id="fbf55-219">As an example, if Outlook has obtained the location code wc:JAXX0085 from Contoso Weather for Tokyo, Outlook uses this location code in the following URL to get the weather information.</span></span>
  
https://service.contoso.com/data.aspx?wealocations=wc:JAXX0085
  
<span data-ttu-id="fbf55-p116">Contoso Météo répond avec le code XML suivant afin de fournir les informations météorologiques correspondant au code d'emplacement de Tokyo. Le code XML est conforme au schéma XML des informations météorologiques d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p116">Contoso Weather responds with the following XML to provide the weather information for the location code for Tokyo. The XML conforms to the Outlook Weather Information XML Schema.</span></span>
  
```XML
<?xml version="1.0"?>
<weatherdata>
  <weather timezone="9" attribution="Data provided by Trey Research" 
    degreetype="F" imagerelativeurl="https://contoso.com/images/en-us/" 
    url="https://contoso.com/weather.aspx?eid=33568&amp;q=Tokyo-JPN" 
    weatherlocationname="Tokyo, JPN" 
    weatherlocationcode="wc:JAXX0085">
      <current winddisplay="9 mph NNW" windspeed="9" humidity="90" feelslike="44" 
        observationpoint="Tokyo" observationtime="06:00:00" 
        shortday="Sat" day="Saturday" date="2012-04-14" skytext="Rain" skycode="11" 
        temperature="48"/>
      <forecast shortday="Sat" day="Saturday" date="2012-04-14" precip="95" skytextday="Rain"
        skycodeday="11" high="55" low="47"/>
      <forecast shortday="Sun" day="Sunday" date="2012-04-15" precip="5" skytextday="Partly Cloudy" 
        skycodeday="30" high="65" low="43"/>
      <forecast shortday="Mon" day="Monday" date="2012-04-16" precip="5" skytextday="Partly Cloudy" 
        skycodeday="30" high="64" low="52"/>
      <forecast shortday="Tue" day="Tuesday" date="2012-04-17" precip="70" skytextday="Showers / Clear" 
        skycodeday="39" high="66" low="53"/>
      <forecast shortday="Wed" day="Wednesday" date="2012-04-18" precip="55" skytextday="Showers / Clear" 
        skycodeday="39" high="68" low="51"/>
  </weather>
</weatherdata>

```

### <a name="resetting-outlook-to-use-msn-weather"></a><span data-ttu-id="fbf55-222">Réinitialisation d'Outlook pour utiliser MSN Météo</span><span class="sxs-lookup"><span data-stu-id="fbf55-222">Resetting Outlook to use MSN Weather</span></span>

<span data-ttu-id="fbf55-p117">Bien qu'Outlook utilise MSN Météo par défaut, si un utilisateur a personnalisé la barre météorologique afin d'utiliser un autre service météo mais par la suite souhaite réutiliser MSN Météo, il peut simplement supprimer la clé **WeatherServiceUrl** du Registre Windows. La suppression de cette clé de Registre réinitialise Outlook afin qu'il utilise MSN Météo.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p117">Even though Outlook uses MSN Weather by default, if a user has customized the Weather Bar to use a different weather service and subsequently wants to use MSN Weather again, the user can simply delete the **WeatherServiceUrl** key in the Windows Registry. Deleting that registry key resets Outlook to use MSN Weather.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="fbf55-225">Conclusion</span><span class="sxs-lookup"><span data-stu-id="fbf55-225">Conclusion</span></span>
<span data-ttu-id="fbf55-226"><a name="ol15_weatherbar_conclusion"> </a></span><span class="sxs-lookup"><span data-stu-id="fbf55-226"><a name="ol15_weatherbar_conclusion"> </a></span></span>

<span data-ttu-id="fbf55-p118">La barre météorologique du calendrier Outlook utilise MSN Météo par défaut pour fournir les prévisions météo d'un emplacement donné. Les utilisateurs peuvent facilement voir les informations relatives à la météo des lieux qui les intéressent. Les services de données météorologiques tiers peuvent également être intégrés à la barre météorologique s'ils prennent en charge le schéma XML d'emplacement météorologique d'Outlook et le schéma des informations météorologiques d'Outlook, et s'ils suivent un protocole de service web simple avec Outlook.</span><span class="sxs-lookup"><span data-stu-id="fbf55-p118">The Weather Bar in the Outlook calendar uses MSN Weather by default to provide the weather forecast for a specified location. Users can conveniently see weather information for the locations they care about. Third-party weather data services can also integrate with the Weather Bar by supporting the Outlook Weather Location XML Schema and Outlook Weather Information XML Schema and following a simple web service protocol with Outlook.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fbf55-230">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf55-230">See also</span></span>

- [<span data-ttu-id="fbf55-231">Schéma XML de lieu météorologique d’Outlook</span><span class="sxs-lookup"><span data-stu-id="fbf55-231">Outlook Weather Location XML Schema</span></span>](outlook-weather-location-xml-schema.md)   
- [<span data-ttu-id="fbf55-232">Outlook Weather Information XML Schema</span><span class="sxs-lookup"><span data-stu-id="fbf55-232">Outlook Weather Information XML Schema</span></span>](outlook-weather-information-xml-schema.md)
    

