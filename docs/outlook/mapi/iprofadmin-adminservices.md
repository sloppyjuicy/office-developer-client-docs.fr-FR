---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422081"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="d6eb3-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="d6eb3-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="d6eb3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6eb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6eb3-105">Permet d’accéder à un objet d’administration de service de message pour apporter des modifications aux services de message dans un profil.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="d6eb3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6eb3-106">Parameters</span></span>

 <span data-ttu-id="d6eb3-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="d6eb3-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="d6eb3-108">[in] Pointeur vers le nom du profil à modifier.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="d6eb3-109">Le  _paramètre lpszProfileName ne_ doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="d6eb3-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="d6eb3-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="d6eb3-111">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="d6eb3-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d6eb3-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="d6eb3-113">[in] Poignée de la fenêtre parente pour toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="d6eb3-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6eb3-114">_ulFlags_</span></span>
  
> <span data-ttu-id="d6eb3-115">[in] Masque de bits d’indicateurs qui contrôle la récupération de l’objet d’administration du service de message.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="d6eb3-116">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="d6eb3-116">The following flags can be set:</span></span>
    
<span data-ttu-id="d6eb3-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d6eb3-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="d6eb3-118">Active l’affichage d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="d6eb3-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6eb3-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d6eb3-120">Le nom du profil est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="d6eb3-121">Si l MAPI_UNICODE n’est pas définie, le nom est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="d6eb3-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="d6eb3-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="d6eb3-123">[out] Pointeur vers un pointeur vers un objet d’administration de service de message.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6eb3-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d6eb3-124">Return value</span></span>

<span data-ttu-id="d6eb3-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6eb3-125">S_OK</span></span> 
  
> <span data-ttu-id="d6eb3-126">L’objet d’administration du service de message a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="d6eb3-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="d6eb3-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="d6eb3-128">Le profil spécifié n’existe pas, ou le mot de passe était incorrect et une boîte de dialogue n’a pas pu être affichée pour demander le mot de passe correct, car MAPI_DIALOG n’a pas été définie dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="d6eb3-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d6eb3-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d6eb3-130">L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6eb3-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6eb3-131">Remarks</span></span>

<span data-ttu-id="d6eb3-132">La **méthode IProfAdmin::AdminServices** permet d’accéder à un objet d’administration de service de message pour apporter des modifications de configuration aux services de message dans un profil.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="d6eb3-133">Le  _paramètre lpszPassword_ doit être NULL ou pointeur vers une chaîne de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d6eb3-134">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="d6eb3-134">Notes to callers</span></span>

<span data-ttu-id="d6eb3-135">Bien que vous pouvez récupérer un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) en appelant cette méthode ou [IMAPISession::AdminServices,](imapisession-adminservices.md)appelez **IProfAdmin::AdminServices** si vous avez strictement un client de configuration et que vous n’offrez aucune fonctionnalité de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="d6eb3-136">**IProfAdmin::AdminServices** ne crée pas d’objet de session et ne charge aucun fournisseur de services, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="d6eb3-137">Vous ne pouvez pas **utiliser IProfAdmin::AdminServices** pour créer un profil.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="d6eb3-138">Par conséquent, vous devez spécifier un profil valide existant dans  _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="d6eb3-139">Si le profil spécifié n’existe pas, **IProfAdmin::AdminServices** renvoie MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="d6eb3-140">Le nom du profil peut comporter jusqu’à 64 caractères et peut inclure les caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="d6eb3-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="d6eb3-141">Tous les caractères alphanumériques, y compris les caractères d’accentuateur et le caractère de soulignement.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="d6eb3-142">Espaces incorporés, mais pas espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d6eb3-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d6eb3-143">MFCMAPI reference</span></span>

<span data-ttu-id="d6eb3-144">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d6eb3-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d6eb3-145">**File**</span></span>|<span data-ttu-id="d6eb3-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d6eb3-146">**Function**</span></span>|<span data-ttu-id="d6eb3-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d6eb3-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6eb3-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d6eb3-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="d6eb3-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="d6eb3-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="d6eb3-150">MFCMAPI utilise la méthode **IProfAdmin::AdminServices** pour ouvrir un objet d’administration de service de message pour le profil sélectionné afin d’ajouter des services.</span><span class="sxs-lookup"><span data-stu-id="d6eb3-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6eb3-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6eb3-151">See also</span></span>



[<span data-ttu-id="d6eb3-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="d6eb3-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="d6eb3-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6eb3-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="d6eb3-154">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d6eb3-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

