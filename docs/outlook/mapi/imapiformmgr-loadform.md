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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1f3a876269868c30df48e0a0b62036cfdc199955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783795"
---
# <a name="imapiformmgrloadform"></a><span data-ttu-id="5c5ca-103">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="5c5ca-103">IMAPIFormMgr::LoadForm</span></span>

  
  
<span data-ttu-id="5c5ca-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c5ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c5ca-105">Démarre un formulaire pour ouvrir un message existant.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-105">Starts a form to open an existing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5c5ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c5ca-106">Parameters</span></span>

 <span data-ttu-id="5c5ca-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5c5ca-108">[in] Un handle vers la fenêtre parent de l’indicateur de progression est affichée pendant que le formulaire est ouvert.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="5c5ca-109">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="5c5ca-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="5c5ca-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5c5ca-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est ouvert.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="5c5ca-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="5c5ca-112">The following flags can be set:</span></span>
    
<span data-ttu-id="5c5ca-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5c5ca-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="5c5ca-114">Affiche une interface utilisateur pour fournir l’état ou demandez à l’utilisateur pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="5c5ca-115">Si cet indicateur n’est pas défini, aucune interface utilisateur est affichée.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-115">If this flag is not set, no user interface is displayed.</span></span>
    
<span data-ttu-id="5c5ca-116">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="5c5ca-116">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="5c5ca-117">Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-117">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="5c5ca-118">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-118">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="5c5ca-119">[in] Pointeur vers une chaîne qui nomme la classe de message du message à charger.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-119">[in] A pointer to a string that names the message class of the message to be loaded.</span></span> <span data-ttu-id="5c5ca-120">Si NULL est indiqué dans le paramètre _lpszMessageClass_ , la classe de message est déterminée à partir du message indiqué par le paramètre _pmsg_ .</span><span class="sxs-lookup"><span data-stu-id="5c5ca-120">If NULL is passed in the  _lpszMessageClass_ parameter, the message class is determined from the message pointed to by the  _pmsg_ parameter.</span></span> 
    
 <span data-ttu-id="5c5ca-121">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-121">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="5c5ca-122">[in] Masque de bits d’indicateurs défini par le client ou défini par le fournisseur copiées à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message qui fournit des informations sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-122">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message that provides information about the state of the message.</span></span> <span data-ttu-id="5c5ca-123">Le paramètre _ulMessageStatus_ doit être défini si _lpszMessageClass_ n’est pas NULL ; Sinon, _ulMessageStatus_ est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-123">The  _ulMessageStatus_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageStatus_ is ignored.</span></span> 
    
 <span data-ttu-id="5c5ca-124">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-124">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="5c5ca-125">[in] Pointeur vers un masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message qui indique l’état actuel du message.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-125">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message that indicates the current state of the message.</span></span> <span data-ttu-id="5c5ca-126">Le paramètre _ulMessageFlags_ doit être défini si _lpszMessageClass_ n’est pas NULL ; Sinon, _ulMessageFlags_ est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-126">The  _ulMessageFlags_ parameter must be set if  _lpszMessageClass_ is non-NULL; otherwise,  _ulMessageFlags_ is ignored.</span></span> 
    
 <span data-ttu-id="5c5ca-127">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-127">_pFolderFocus_</span></span>
  
> <span data-ttu-id="5c5ca-128">[in] Pointeur vers le dossier qui contient directement le message.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-128">[in] A pointer to the folder that directly contains the message.</span></span> <span data-ttu-id="5c5ca-129">Le paramètre _pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message).</span><span class="sxs-lookup"><span data-stu-id="5c5ca-129">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
 <span data-ttu-id="5c5ca-130">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-130">_pMessageSite_</span></span>
  
> <span data-ttu-id="5c5ca-131">[in] Pointeur vers le site de message du message.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-131">[in] A pointer to the message site of the message.</span></span>
    
 <span data-ttu-id="5c5ca-132">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-132">_pmsg_</span></span>
  
> <span data-ttu-id="5c5ca-133">[in] Pointeur vers le message.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-133">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="5c5ca-134">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-134">_pViewContext_</span></span>
  
> <span data-ttu-id="5c5ca-135">[in] Pointeur vers le contexte d’affichage pour le message.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-135">[in] A pointer to the view context for the message.</span></span> <span data-ttu-id="5c5ca-136">Le paramètre _pViewContext_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-136">The  _pViewContext_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5c5ca-137">_riid_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-137">_riid_</span></span>
  
> <span data-ttu-id="5c5ca-138">[in] L’identificateur d’interface (IID) de l’interface à utiliser pour l’objet de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-138">[in] The interface identifier (IID) of the interface to be used for the returned form object.</span></span> <span data-ttu-id="5c5ca-139">Le paramètre _riid_ ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-139">The  _riid_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="5c5ca-140">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="5c5ca-140">_ppvObj_</span></span>
  
> <span data-ttu-id="5c5ca-141">[out] Pointeur vers un pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-141">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c5ca-142">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="5c5ca-142">Return value</span></span>

<span data-ttu-id="5c5ca-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c5ca-143">S_OK</span></span> 
  
> <span data-ttu-id="5c5ca-144">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-144">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5c5ca-145">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="5c5ca-145">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="5c5ca-146">Le formulaire ne prend pas en charge l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-146">The form does not support the requested interface.</span></span>
    
<span data-ttu-id="5c5ca-147">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5c5ca-147">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5c5ca-148">La classe de message passée dans _lpszMessageClass_ ne correspond pas à la classe de message pour n’importe quel formulaire dans la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-148">The message class passed in  _lpszMessageClass_ does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c5ca-149">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c5ca-149">Remarks</span></span>

<span data-ttu-id="5c5ca-150">Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::LoadForm** pour ouvrir un formulaire pour un message existant.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-150">Form viewers call the **IMAPIFormMgr::LoadForm** method to open a form for an existing message.</span></span> <span data-ttu-id="5c5ca-151">**LoadForm** ouvre l’objet de formulaire, charge le message dans l’objet de formulaire, définit le contexte de vue appropriée, si nécessaire et renvoie l’interface demandée pour l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-151">**LoadForm** opens the form object, loads the message into the form object, sets up the appropriate view context, if necessary, and returns the requested interface for the form object.</span></span> 
  
<span data-ttu-id="5c5ca-152">Le paramètre _pFolderFocus_ pointe vers le dossier qui contient le message.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-152">The  _pFolderFocus_ parameter points to the folder that contains the message.</span></span> <span data-ttu-id="5c5ca-153">Si le message est incorporé dans un autre message, _pFolderFocus_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-153">If the message is embedded in another message,  _pFolderFocus_ should be NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5c5ca-154">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="5c5ca-154">Notes to implementers</span></span>

<span data-ttu-id="5c5ca-155">Si NULL est indiqué dans _lpszMessageClass_, l’implémentation Obtient la classe de message du message, l’état et d’indicateurs à partir du message **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** et **PR_MESSAGE_FLAGS **propriétés.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-155">If NULL is passed in  _lpszMessageClass_, the implementation obtains the message's message class, status, and flags from the message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** and **PR_MESSAGE_FLAGS** properties.</span></span> <span data-ttu-id="5c5ca-156">Si une chaîne de classe de message est fournie dans _lpszMessageClass_, l’implémentation doit utiliser les valeurs _ulMessageStatus_ et _ulMessageFlags_.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-156">If a message class string is provided in  _lpszMessageClass_, the implementation must use the values in  _ulMessageStatus_ and  _ulMessageFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5c5ca-157">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5c5ca-157">MFCMAPI reference</span></span>

<span data-ttu-id="5c5ca-158">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-158">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5c5ca-159">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5c5ca-159">**File**</span></span>|<span data-ttu-id="5c5ca-160">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5c5ca-160">**Function**</span></span>|<span data-ttu-id="5c5ca-161">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5c5ca-161">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c5ca-162">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5c5ca-162">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5c5ca-163">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="5c5ca-163">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="5c5ca-164">MFCMAPI utilise la méthode **IMAPIFormMgr::LoadForm** pour charger un formulaire avant de les afficher.</span><span class="sxs-lookup"><span data-stu-id="5c5ca-164">MFCMAPI uses the **IMAPIFormMgr::LoadForm** method to load a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c5ca-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c5ca-165">See also</span></span>



[<span data-ttu-id="5c5ca-166">Propriété canonique PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="5c5ca-166">PidTagMessageClass Canonical Property</span></span>](pidtagmessageclass-canonical-property.md)
  
[<span data-ttu-id="5c5ca-167">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="5c5ca-167">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="5c5ca-168">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="5c5ca-168">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="5c5ca-169">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c5ca-169">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="5c5ca-170">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5c5ca-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

