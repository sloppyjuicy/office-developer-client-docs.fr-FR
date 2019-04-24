---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317396"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="45be9-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="45be9-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="45be9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45be9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45be9-105">Déconseillé: l'utilisation de [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) est recommandée.</span><span class="sxs-lookup"><span data-stu-id="45be9-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="45be9-106">Ajoute un service de messagerie au profil actif.</span><span class="sxs-lookup"><span data-stu-id="45be9-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="45be9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45be9-107">Parameters</span></span>

 <span data-ttu-id="45be9-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="45be9-108">_lpszService_</span></span>
  
> <span data-ttu-id="45be9-109">dans Pointeur vers le nom du service de messagerie à ajouter.</span><span class="sxs-lookup"><span data-stu-id="45be9-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="45be9-110">Ce nom de service de message doit apparaître dans la section **[services]** du fichier MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="45be9-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="45be9-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="45be9-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="45be9-112">dans Pointeur vers le nom d'affichage du service de messagerie à ajouter.</span><span class="sxs-lookup"><span data-stu-id="45be9-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="45be9-113">Le paramètre _lpszDisplayName_ est ignoré si le service de messagerie a défini la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans le fichier MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="45be9-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="45be9-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="45be9-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="45be9-115">dans Handle de la fenêtre parente de toutes les boîtes de dialogue ou fenêtres que cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="45be9-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="45be9-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45be9-116">_ulFlags_</span></span>
  
> <span data-ttu-id="45be9-117">dans Masque de des indicateurs qui contrôle le mode d'installation du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="45be9-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="45be9-118">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="45be9-118">The following flags can be set:</span></span>
    
<span data-ttu-id="45be9-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45be9-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="45be9-120">Les paramètres lpszService et lpszDisplayName doivent être castés en LPWSTR et interprétés comme des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="45be9-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="45be9-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="45be9-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="45be9-122">Lors de l'ajout d'un nouveau service de messagerie au profil, le sous-système MAPI, basé sur différentes circonstances et critères, détermine souvent que cette action nécessite un redémarrage d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="45be9-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="45be9-123">Si l'indicateur SERVICE_NO_RESTART_WARNING n'est pas inclus et que l'interface utilisateur est autorisée (en fonction des indicateurs SERVICE_UI_ALWAYS et SERVICE_UI_ALLOWED) et qu'au moins un processus est connecté au profil actuel, cette fonction affiche le message «vous devez redémarrer Outlook pour Ces modifications prennent effet. "</span><span class="sxs-lookup"><span data-stu-id="45be9-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="45be9-124">L'ajout de l'indicateur SERVICE_NO_RESTART_WARNING supprime l'affichage de ce message d'avertissement.</span><span class="sxs-lookup"><span data-stu-id="45be9-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="45be9-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="45be9-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="45be9-126">L'interface utilisateur de configuration du service de messagerie est autorisée si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="45be9-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="45be9-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="45be9-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="45be9-128">Le service de messagerie affiche sa feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="45be9-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45be9-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="45be9-129">Return value</span></span>

<span data-ttu-id="45be9-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="45be9-130">S_OK</span></span> 
  
> <span data-ttu-id="45be9-131">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="45be9-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="45be9-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="45be9-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="45be9-133">Le nom du service de messagerie ne figure pas dans la section **[services]** du fichier MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="45be9-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="45be9-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="45be9-134">Remarks</span></span>

<span data-ttu-id="45be9-135">La méthode **IMsgServiceAdmin:: CreateMsgService** ajoute un service de messagerie au profil actif.</span><span class="sxs-lookup"><span data-stu-id="45be9-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="45be9-136">**CreateMsgService** appelle la fonction de point d'entrée du service de messagerie pour effectuer les tâches de configuration propres au service.</span><span class="sxs-lookup"><span data-stu-id="45be9-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="45be9-137">Si l'indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ , le service de messagerie en cours d'installation peut afficher une feuille de propriétés pour permettre à l'utilisateur de configurer ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="45be9-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="45be9-138">Le fichier MapiSvc. INF contient la liste des fournisseurs qui composent un service de messagerie et les propriétés de chacune d'elles.</span><span class="sxs-lookup"><span data-stu-id="45be9-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="45be9-139">**CreateMsgService** crée d'abord une section de profil pour le service de messagerie, puis copie toutes les informations pour ce service à partir du fichier MapiSvc. inf dans le profil, créant de nouvelles sections pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="45be9-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="45be9-140">Une fois que toutes les informations ont été copiées à partir de MapiSvc. inf, la fonction de point d'entrée du service de messagerie est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="45be9-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="45be9-141">Si l'indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ de la méthode **CreateMsgService** , les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises lors de l'appel à la fonction point d'entrée du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="45be9-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="45be9-142">Les fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs puissent configurer le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="45be9-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="45be9-143">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="45be9-143">Notes to callers</span></span>

 <span data-ttu-id="45be9-144">**CreateMsgService** ne retourne pas la structure [MAPIUID](mapiuid.md) pour le service de messagerie qui a été ajouté au profil.</span><span class="sxs-lookup"><span data-stu-id="45be9-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="45be9-145">Pour récupérer le **MAPIUID** pour le service de messagerie créé, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="45be9-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="45be9-146">Appelez la méthode [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour obtenir la table d'administration des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="45be9-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="45be9-147">Localisez la ligne qui représente le service de messagerie en plaçant une restriction sur la table qui correspond à la propriété **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) avec le nom du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="45be9-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="45be9-148">Récupérez la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service.</span><span class="sxs-lookup"><span data-stu-id="45be9-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="45be9-149">TransMettez la valeur de la propriété **PR_SERVICE_UID** dans le paramètre _lpUid_ à la méthode [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service.</span><span class="sxs-lookup"><span data-stu-id="45be9-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="45be9-150">L'implémentation Microsoft Outlook 2010 du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échoue si elle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="45be9-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="45be9-151">Le _ulFlags_ SERVICE_NO_RESTART_WARNING peut ne pas être défini dans le fichier d'en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l'ajouter à votre code à l'aide de la valeur suivante: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="45be9-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="45be9-152">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="45be9-152">MFCMAPI reference</span></span>

<span data-ttu-id="45be9-153">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="45be9-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="45be9-154">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="45be9-154">**File**</span></span>|<span data-ttu-id="45be9-155">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="45be9-155">**Function**</span></span>|<span data-ttu-id="45be9-156">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="45be9-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45be9-157">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="45be9-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="45be9-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="45be9-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="45be9-159">MFCMAPI utilise la méthode **IMsgServiceAdmin:: CreateMsgService** pour ajouter un service à un profil.</span><span class="sxs-lookup"><span data-stu-id="45be9-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45be9-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45be9-160">See also</span></span>



[<span data-ttu-id="45be9-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45be9-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="45be9-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="45be9-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

