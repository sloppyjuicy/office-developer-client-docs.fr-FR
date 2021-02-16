---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418784"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="ee0da-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="ee0da-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="ee0da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee0da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee0da-105">Démarre un formulaire pour ouvrir un message existant.</span><span class="sxs-lookup"><span data-stu-id="ee0da-105">Starts a form to open an existing message.</span></span>
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="ee0da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee0da-106">Parameters</span></span>

 <span data-ttu-id="ee0da-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ee0da-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="ee0da-108">[in] Poignée vers la fenêtre parente de l’indicateur de progression qui s’affiche pendant l’ouverture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ee0da-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="ee0da-109">Le _paramètre ulUIParam_ est ignoré, sauf si l’MAPI_DIALOG est définie dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ee0da-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ee0da-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee0da-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ee0da-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est ouvert.</span><span class="sxs-lookup"><span data-stu-id="ee0da-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="ee0da-112">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="ee0da-112">The following flags can be set:</span></span>
    
<span data-ttu-id="ee0da-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ee0da-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="ee0da-114">Affiche une interface utilisateur pour fournir un état ou invite l’utilisateur à fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ee0da-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="ee0da-115">Si cet indicateur n’est pas définie, aucune interface utilisateur n’est affichée.</span><span class="sxs-lookup"><span data-stu-id="ee0da-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="ee0da-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="ee0da-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="ee0da-117">Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.</span><span class="sxs-lookup"><span data-stu-id="ee0da-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="ee0da-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="ee0da-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="ee0da-119">[in] Pointeur vers une chaîne qui nomme la classe de message du message à charger.</span><span class="sxs-lookup"><span data-stu-id="ee0da-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="ee0da-120">Si NULL est transmis dans le paramètre _lpszMessageClass,_ la classe de message est déterminée à partir du message pointé par le _paramètre pmsg._</span><span class="sxs-lookup"><span data-stu-id="ee0da-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="ee0da-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="ee0da-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="ee0da-122">[in] Masque de bits d’indicateurs définis par le client ou par un fournisseur copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message qui fournit des informations sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="ee0da-123">Le  _paramètre ulMessageStatus_ doit être paramétrage si  _lpszMessageClass_ n’est pas NULL ; Dans le  _cas contraire, ulMessageStatus_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ee0da-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="ee0da-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="ee0da-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="ee0da-125">[in] Pointeur vers un masque de bits d’indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message qui indique l’état actuel du message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="ee0da-126">Le  _paramètre ulMessageFlags doit_ être paramétrage si  _lpszMessageClass_ est non NULL ; Dans le  _cas contraire, ulMessageFlags_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ee0da-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="ee0da-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="ee0da-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="ee0da-128">[in] Pointeur vers le dossier qui contient directement le message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="ee0da-129">Le  _paramètre pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message).</span><span class="sxs-lookup"><span data-stu-id="ee0da-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="ee0da-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="ee0da-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="ee0da-131">[in] Pointeur vers le site de message du message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="ee0da-132">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="ee0da-132">_pmsg_</span></span>
  
> <span data-ttu-id="ee0da-133">[in] Pointeur vers le message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="ee0da-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="ee0da-134">_pViewContext_</span></span>
  
> <span data-ttu-id="ee0da-135">[in] Pointeur vers le contexte d’affichage du message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="ee0da-136">Le  _paramètre pViewContext_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="ee0da-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ee0da-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="ee0da-137">_riid_</span></span>
  
> <span data-ttu-id="ee0da-138">[in] Identificateur d’interface (IID) de l’interface à utiliser pour l’objet de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="ee0da-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="ee0da-139">Le  _paramètre riid_ ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="ee0da-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="ee0da-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="ee0da-140">_ppvObj_</span></span>
  
> <span data-ttu-id="ee0da-141">[out] Pointeur vers un pointeur vers l’interface renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ee0da-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee0da-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ee0da-142">Return value</span></span>

<span data-ttu-id="ee0da-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee0da-143">S_OK</span></span> 
  
> <span data-ttu-id="ee0da-144">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ee0da-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ee0da-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ee0da-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="ee0da-146">Le formulaire ne prend pas en charge l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="ee0da-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="ee0da-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ee0da-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ee0da-148">La classe de message transmise dans  _lpszMessageClass_ ne correspond à la classe de message pour aucun formulaire de la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="ee0da-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ee0da-149">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee0da-149">Remarks</span></span>

<span data-ttu-id="ee0da-150">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::LoadForm** pour ouvrir un formulaire pour un message existant.</span><span class="sxs-lookup"><span data-stu-id="ee0da-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="ee0da-151">**LoadForm** ouvre l’objet formulaire, charge le message dans l’objet formulaire, définit le contexte d’affichage approprié, si nécessaire, et renvoie l’interface demandée pour l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ee0da-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="ee0da-152">Le  _paramètre pFolderFocus_ pointe vers le dossier qui contient le message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="ee0da-153">Si le message est incorporé dans un autre message,  _pFolderFocus_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="ee0da-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ee0da-154">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ee0da-154">Notes to implementers</span></span>

<span data-ttu-id="ee0da-155">Si LA VALEUR NULL est passée dans  _lpszMessageClass,_ l’implémentation obtient la classe de message, l’état et les indicateurs du message à partir des propriétés **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** et **PR_MESSAGE_FLAGS** du message.</span><span class="sxs-lookup"><span data-stu-id="ee0da-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="ee0da-156">Si une chaîne de classe de message est fournie dans  _lpszMessageClass_, l’implémentation doit utiliser les valeurs dans  _ulMessageStatus_ et  _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="ee0da-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ee0da-157">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ee0da-157">MFCMAPI reference</span></span>

<span data-ttu-id="ee0da-158">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ee0da-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ee0da-159">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ee0da-159">**File**</span></span>|<span data-ttu-id="ee0da-160">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ee0da-160">**Function**</span></span>|<span data-ttu-id="ee0da-161">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ee0da-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee0da-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ee0da-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ee0da-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="ee0da-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="ee0da-164">MFCMAPI utilise la **méthode IMAPIFormMgr::LoadForm** pour charger un formulaire avant de l’afficher.</span><span class="sxs-lookup"><span data-stu-id="ee0da-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee0da-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee0da-165">See also</span></span>



[<span data-ttu-id="ee0da-166">Propriété canonique PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="ee0da-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="ee0da-167">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="ee0da-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="ee0da-168">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ee0da-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="ee0da-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee0da-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="ee0da-170">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ee0da-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

