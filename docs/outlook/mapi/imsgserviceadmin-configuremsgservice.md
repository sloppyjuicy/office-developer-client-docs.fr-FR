---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a599a6fe5093e52e50d33a1761df5689b7335138
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568293"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="fab18-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="fab18-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="fab18-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fab18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fab18-105">RECONFIGURE un service de message.</span><span class="sxs-lookup"><span data-stu-id="fab18-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="fab18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fab18-106">Parameters</span></span>

 <span data-ttu-id="fab18-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="fab18-107">_lpUID_</span></span>
  
> <span data-ttu-id="fab18-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message à configurer.</span><span class="sxs-lookup"><span data-stu-id="fab18-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="fab18-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fab18-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="fab18-110">[in] Un handle vers la fenêtre parent de la feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="fab18-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="fab18-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fab18-111">_ulFlags_</span></span>
  
> <span data-ttu-id="fab18-112">[in] Masque de bits d’indicateurs qui contrôle l’affichage de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fab18-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="fab18-113">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="fab18-113">The following flags can be set:</span></span>
    
<span data-ttu-id="fab18-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fab18-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fab18-115">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="fab18-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="fab18-116">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="fab18-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="fab18-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="fab18-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="fab18-118">Le service de message doit afficher sa feuille de propriétés de configuration, mais pas permettre à l’utilisateur à modifier.</span><span class="sxs-lookup"><span data-stu-id="fab18-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="fab18-119">La plupart des services de messagerie ignorent cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="fab18-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="fab18-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="fab18-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="fab18-121">Le service de message doit afficher sa feuille de propriétés de configuration uniquement si le service n’est pas entièrement configuré.</span><span class="sxs-lookup"><span data-stu-id="fab18-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="fab18-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="fab18-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="fab18-123">Le service de message doit toujours afficher sa feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="fab18-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="fab18-124">Si SERVICE_UI_ALWAYS n’est pas défini, une feuille de propriétés de configuration peut toujours être affichée si SERVICE_UI_ALLOWED est défini et les informations de configuration valides ne sont pas disponibles dans le tableau de valeurs de propriété dans le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="fab18-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="fab18-125">SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS doit être définie pour une feuille de propriétés à afficher.</span><span class="sxs-lookup"><span data-stu-id="fab18-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="fab18-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="fab18-126">_cValues_</span></span>
  
> <span data-ttu-id="fab18-127">[in] Le nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) désignés par _lpProps_.</span><span class="sxs-lookup"><span data-stu-id="fab18-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="fab18-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="fab18-128">_lpProps_</span></span>
  
> <span data-ttu-id="fab18-129">[in] Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à afficher dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="fab18-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="fab18-130">Le paramètre _lpProps_ ne doit pas être NULL si le service de message doit être configuré sans interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fab18-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fab18-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fab18-131">Return value</span></span>

<span data-ttu-id="fab18-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="fab18-132">S_OK</span></span> 
  
> <span data-ttu-id="fab18-133">Le service de message a été correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="fab18-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="fab18-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="fab18-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="fab18-135">Une erreur spécifique à un service de message.</span><span class="sxs-lookup"><span data-stu-id="fab18-135">An error specific to a message service.</span></span> <span data-ttu-id="fab18-136">Pour obtenir la structure [MAPIERROR](mapierror.md) qui décrit l’erreur, l’application cliente doit appeler la méthode [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fab18-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="fab18-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fab18-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fab18-138">Le **MAPIUID** désignés par _lpUID_ ne correspond pas à celui d’un service de message existant.</span><span class="sxs-lookup"><span data-stu-id="fab18-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="fab18-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="fab18-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="fab18-140">Le service message n’a pas d’entrée de fonction de point.</span><span class="sxs-lookup"><span data-stu-id="fab18-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="fab18-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="fab18-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="fab18-142">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="fab18-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fab18-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="fab18-143">Remarks</span></span>

<span data-ttu-id="fab18-144">La méthode **IMsgServiceAdmin::ConfigureMsgService** permet à un service de message à configurer, avec ou sans une feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="fab18-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="fab18-145">Pour permettre la configuration sans un affichage feuille des propriétés, services message préparent généralement un fichier d’en-tête qui contient des constantes pour toutes les propriétés obligatoires et facultatifs et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="fab18-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="fab18-146">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="fab18-146">Notes to callers</span></span>

<span data-ttu-id="fab18-147">Pour récupérer la structure **MAPIUID** pour le service de message configurer, récupérer la colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="fab18-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="fab18-148">Pour plus d’informations, voir la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fab18-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="fab18-149">Vous pouvez configurer un service de message sans afficher une feuille de propriétés à un utilisateur uniquement si vous disposez des informations supplémentaires sur les valeurs de propriété à définir.</span><span class="sxs-lookup"><span data-stu-id="fab18-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="fab18-150">Si vous configurez un service de message sans afficher une feuille de propriétés, passer des valeurs de propriété valide dans le paramètre _lpProps_ et ne définissez pas les indicateurs MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="fab18-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="fab18-151">Si vous recevez tout ou partie des informations de configuration de l’utilisateur par une feuille de propriétés, définissez SERVICE_UI_ALLOWED dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="fab18-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="fab18-152">Si vous utilisez les informations de propriété existantes uniquement établir des paramètres par défaut et l’utilisateur est en mesure de modifier les paramètres, définissez SERVICE_UI_ALWAYS dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="fab18-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fab18-153">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fab18-153">MFCMAPI reference</span></span>

<span data-ttu-id="fab18-154">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fab18-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fab18-155">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="fab18-155">**File**</span></span>|<span data-ttu-id="fab18-156">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="fab18-156">**Function**</span></span>|<span data-ttu-id="fab18-157">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="fab18-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fab18-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fab18-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fab18-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="fab18-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="fab18-160">MFCMAPI utilise la méthode **IMsgServiceAdmin::ConfigureMsgService** pour configurer un service qui a été ajouté à un profil.</span><span class="sxs-lookup"><span data-stu-id="fab18-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fab18-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fab18-161">See also</span></span>



[<span data-ttu-id="fab18-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fab18-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="fab18-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fab18-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="fab18-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fab18-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="fab18-165">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="fab18-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

