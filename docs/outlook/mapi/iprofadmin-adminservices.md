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
ms.openlocfilehash: a9e596ff8561d5aabc71ffe3540efaeef8f5b83d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593983"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="c4e9b-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="c4e9b-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="c4e9b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4e9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4e9b-105">Donne accès à un objet de l’administration de service de message pour apporter des modifications aux services de message dans un profil.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="c4e9b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4e9b-106">Parameters</span></span>

 <span data-ttu-id="c4e9b-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="c4e9b-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="c4e9b-108">[in] Pointeur vers le nom du profil à modifier.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="c4e9b-109">Le paramètre _lpszProfileName_ ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="c4e9b-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="c4e9b-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="c4e9b-111">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="c4e9b-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c4e9b-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="c4e9b-113">[in] Handle de la fenêtre parente pour les boîtes de dialogue ou windows qui affiche cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="c4e9b-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c4e9b-114">_ulFlags_</span></span>
  
> <span data-ttu-id="c4e9b-115">[in] Masque de bits d’indicateurs qui contrôle la récupération de l’objet de l’administration du service de message.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="c4e9b-116">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="c4e9b-116">The following flags can be set:</span></span>
    
<span data-ttu-id="c4e9b-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c4e9b-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="c4e9b-118">Active l’affichage d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="c4e9b-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4e9b-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c4e9b-120">Le nom de profil est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="c4e9b-121">Si l’indicateur MAPI_UNICODE n’est pas définie, le nom est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="c4e9b-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="c4e9b-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="c4e9b-123">[out] Pointeur vers un pointeur vers un objet de l’administration de service de message.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4e9b-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4e9b-124">Return value</span></span>

<span data-ttu-id="c4e9b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4e9b-125">S_OK</span></span> 
  
> <span data-ttu-id="c4e9b-126">L’objet de l’administration du service de message a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="c4e9b-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="c4e9b-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="c4e9b-128">Le profil spécifié n’existe pas, ou le mot de passe est incorrecte et une boîte de dialogue ne peut pas être affichée à l’utilisateur de demander le mot de passe, car MAPI_DIALOG n’a pas été défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="c4e9b-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c4e9b-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c4e9b-130">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c4e9b-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="c4e9b-131">Remarks</span></span>

<span data-ttu-id="c4e9b-132">La méthode **IProfAdmin::AdminServices** permet d’accéder à un objet de l’administration de service de message pour apporter des modifications de configuration pour les services de messagerie dans un profil.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="c4e9b-133">Le paramètre _lpszPassword_ doit être NULL ou un pointeur vers une chaîne de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c4e9b-134">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c4e9b-134">Notes to callers</span></span>

<span data-ttu-id="c4e9b-135">Bien que vous pouvez récupérer un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) en appelant cette méthode ou [IMAPISession::AdminServices](imapisession-adminservices.md), appelez **IProfAdmin::AdminServices** si vous avez strictement un client de configuration et n’offre aucune des fonctionnalités de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="c4e9b-136">**IProfAdmin::AdminServices** ne crée pas d’un objet de la session et ne se charge pas les fournisseurs de services, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="c4e9b-137">Vous ne pouvez pas utiliser **IProfAdmin::AdminServices** pour créer un profil.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="c4e9b-138">Par conséquent, vous devez spécifier un profil existant valid dans _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="c4e9b-139">Si le profil spécifié n’existe pas, **IProfAdmin::AdminServices** renvoie MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="c4e9b-140">Le nom du profil peut être jusqu'à 64 caractères et peut inclure les caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="c4e9b-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="c4e9b-141">Tous les caractères alphanumériques, y compris les caractères d’accentuation et le caractère de soulignement.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="c4e9b-142">Des espaces, mais pas espaces à gauche ou.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c4e9b-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c4e9b-143">MFCMAPI reference</span></span>

<span data-ttu-id="c4e9b-144">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c4e9b-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c4e9b-145">**File**</span></span>|<span data-ttu-id="c4e9b-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c4e9b-146">**Function**</span></span>|<span data-ttu-id="c4e9b-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c4e9b-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c4e9b-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c4e9b-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="c4e9b-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="c4e9b-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="c4e9b-150">MFCMAPI utilise la méthode **IProfAdmin::AdminServices** pour ouvrir un objet de l’administration de service de message pour le profil sélectionné Ajouter des services.</span><span class="sxs-lookup"><span data-stu-id="c4e9b-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4e9b-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4e9b-151">See also</span></span>



[<span data-ttu-id="c4e9b-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="c4e9b-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="c4e9b-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4e9b-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="c4e9b-154">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c4e9b-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

