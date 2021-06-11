---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410181"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="596c5-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="596c5-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="596c5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="596c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="596c5-105">Ajoute un service de message au profil actuel et renvoie l’UID du service nouvellement ajouté.</span><span class="sxs-lookup"><span data-stu-id="596c5-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="596c5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="596c5-106">Parameters</span></span>

 <span data-ttu-id="596c5-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="596c5-107">_lpszService_</span></span>
  
> <span data-ttu-id="596c5-108">[in] Pointeur vers le nom du service de message à ajouter.</span><span class="sxs-lookup"><span data-stu-id="596c5-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="596c5-109">Ce nom de service de message doit apparaître dans la section **[Services]** du fichier MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="596c5-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="596c5-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="596c5-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="596c5-111">[in] Pointeur vers le nom complet du service de message à ajouter.</span><span class="sxs-lookup"><span data-stu-id="596c5-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="596c5-112">Le  _paramètre lpszDisplayName_ est ignoré si le service de message a définie la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans le fichier MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="596c5-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="596c5-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="596c5-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="596c5-114">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="596c5-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="596c5-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="596c5-115">_ulFlags_</span></span>
  
> <span data-ttu-id="596c5-116">[in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est installé.</span><span class="sxs-lookup"><span data-stu-id="596c5-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="596c5-117">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="596c5-117">The following flags can be set:</span></span>
    
<span data-ttu-id="596c5-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="596c5-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="596c5-119">Les paramètres lpszService et lpszDisplayName doivent être casté vers LPWSTR et interprétés comme des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="596c5-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="596c5-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="596c5-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="596c5-121">Lors de l’ajout d’un nouveau service de message au profil, le sous-système MAPI, en fonction de diverses circonstances et critères, détermine souvent que cette action nécessite un redémarrage Outlook.</span><span class="sxs-lookup"><span data-stu-id="596c5-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="596c5-122">Si l’indicateur SERVICE_NO_RESTART_WARNING n’est pas inclus et que l’interface utilisateur est autorisée (en fonction des indicateurs SERVICE_UI_ALWAYS et SERVICE_UI_ALLOWED) et qu’au moins un processus est connecté au profil actuel, cette fonction affiche le message « Vous devez redémarrer Outlook pour que ces modifications prennent effet ».</span><span class="sxs-lookup"><span data-stu-id="596c5-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="596c5-123">L’SERVICE_NO_RESTART_WARNING’indicateur supprime l’affichage de ce message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="596c5-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="596c5-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="596c5-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="596c5-125">L’interface utilisateur de configuration du service de message est autorisée si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="596c5-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="596c5-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="596c5-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="596c5-127">Le service de message affiche sa feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="596c5-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="596c5-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="596c5-128">_lpuidService_</span></span>
  
> <span data-ttu-id="596c5-129">[out] Pointeur vers l’UID du service de message ajouté.</span><span class="sxs-lookup"><span data-stu-id="596c5-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="596c5-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="596c5-130">Return value</span></span>

<span data-ttu-id="596c5-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="596c5-131">S_OK</span></span>
  
> <span data-ttu-id="596c5-132">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="596c5-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="596c5-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="596c5-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="596c5-134">Le nom du service de message ne se trouve pas dans la section **[Services]** de MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="596c5-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="596c5-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="596c5-135">Remarks</span></span>

<span data-ttu-id="596c5-136">La **méthode IMsgServiceAdmin2::CreateMsgServiceEx** ajoute un service de message au profil actuel.</span><span class="sxs-lookup"><span data-stu-id="596c5-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="596c5-137">**CreateMsgServiceEx** appelle la fonction de point d’entrée du service de message pour effectuer des tâches de configuration spécifiques au service.</span><span class="sxs-lookup"><span data-stu-id="596c5-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="596c5-138">Si l’SERVICE_UI_ALLOWED est définie dans le paramètre  _ulFlags,_ le service de message en cours d’installation peut afficher une feuille de propriétés permettant à l’utilisateur de configurer ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="596c5-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="596c5-139">Le fichier MapiSvc.inf contient la liste des fournisseurs qui font un service de messagerie et les propriétés de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="596c5-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="596c5-140">**CreateMsgServiceEx** crée d’abord une section de profil pour le service de message, puis copie toutes les informations de ce service à partir du fichier MapiSvc.inf dans le profil, créant ainsi de nouvelles sections pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="596c5-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="596c5-141">Une fois toutes les informations copiées à partir de MapiSvc.inf, la fonction de point d’entrée du service de message, **MSGSERVICEENTRY**, est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext._</span><span class="sxs-lookup"><span data-stu-id="596c5-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="596c5-142">Si l’indicateur SERVICE_UI_ALLOWED est définie dans le paramètre _ulFlags_ de la méthode **CreateMsgServiceEx,** les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises lorsque la fonction de point d’entrée du service de message est appelée.</span><span class="sxs-lookup"><span data-stu-id="596c5-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="596c5-143">Les fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs peuvent configurer le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="596c5-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="596c5-144">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="596c5-144">Notes to callers</span></span>

<span data-ttu-id="596c5-145">Si l’argument **CreateMsgServiceEx** _lpuidService_ n’est pas NULL, la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de message ajouté au profil est renvoyée dans le **GUID** vers lequel elle pointe.</span><span class="sxs-lookup"><span data-stu-id="596c5-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="596c5-146">Passez la valeur de la **propriété PR_SERVICE_UID** dans le paramètre  _lpuidService_ à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service.</span><span class="sxs-lookup"><span data-stu-id="596c5-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="596c5-147">L Microsoft Outlook 2010'implémentation du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échouera s’il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="596c5-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="596c5-148">L’interface IMsgServiceAdmin2 est exposée par le même objet qui implémente l’interface IMsgServiceAdmin et est disponible à l’aide de l’implémentation de Outlook du sous-système MAPI depuis Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="596c5-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="596c5-149">Son IID est défini comme suit : >> Le `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);` SERVICE_NO_RESTART_WARNING _ulFlags_ peut ne pas être défini dans le fichier d’en-tête téléchargeable dont vous disposez, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="596c5-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="596c5-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="596c5-150">See also</span></span>



[<span data-ttu-id="596c5-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="596c5-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="596c5-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="596c5-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

