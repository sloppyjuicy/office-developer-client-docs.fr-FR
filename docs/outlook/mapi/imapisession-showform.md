---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783956"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="4d42c-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="4d42c-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="4d42c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d42c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d42c-105">Affiche un formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d42c-105">Displays a form.</span></span>
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="4d42c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d42c-106">Parameters</span></span>

 <span data-ttu-id="4d42c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4d42c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4d42c-108">[in] Un handle vers la fenêtre parent du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d42c-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="4d42c-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="4d42c-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="4d42c-110">[in] Un pointeur vers la banque de messages qui contient le dossier indiqué par le paramètre _lpParentFolder_ .</span><span class="sxs-lookup"><span data-stu-id="4d42c-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="4d42c-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="4d42c-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="4d42c-112">[in] Pointeur vers le dossier dans lequel le message associé au paramètre _ulMessageToken_ a été créé.</span><span class="sxs-lookup"><span data-stu-id="4d42c-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="4d42c-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4d42c-113">_lpInterface_</span></span>
  
> <span data-ttu-id="4d42c-114">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message qui s’affiche dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d42c-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="4d42c-115">Le paramètre _lpInterface_ doit être NULL ou IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="4d42c-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="4d42c-116">Résultats de la transmission NULL dans l’interface standard, [IMessage](imessageimapiprop.md), utilisé.</span><span class="sxs-lookup"><span data-stu-id="4d42c-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="4d42c-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="4d42c-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="4d42c-118">[in] Le jeton qui est associé avec le message à afficher dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d42c-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="4d42c-119">Le paramètre _ulMessageToken_ doit avoir le contenu du paramètre _lpulMessageToken_ à partir de l’appel précédent à [IMAPISession::PrepareForm](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="4d42c-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="4d42c-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="4d42c-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="4d42c-121">[in] Réservé ; doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="4d42c-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="4d42c-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d42c-122">_ulFlags_</span></span>
  
> <span data-ttu-id="4d42c-123">[in] Masque de bits d’indicateurs qui contrôle comment et si le message est enregistré.</span><span class="sxs-lookup"><span data-stu-id="4d42c-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="4d42c-124">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="4d42c-124">The following flags can be set:</span></span>
    
<span data-ttu-id="4d42c-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4d42c-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="4d42c-126">Le message n’a jamais été enregistré (autrement dit, la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) a jamais été appelée).</span><span class="sxs-lookup"><span data-stu-id="4d42c-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="4d42c-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4d42c-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="4d42c-128">Le message doit être enregistré dans son dossier parent.</span><span class="sxs-lookup"><span data-stu-id="4d42c-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="4d42c-129">Le message n’est pas traité pour l’envoi, mais est publié dans le dossier à la place.</span><span class="sxs-lookup"><span data-stu-id="4d42c-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="4d42c-130">Si cet indicateur n’est pas défini, le message est copié dans la boîte d’envoi et est traité pour l’envoi.</span><span class="sxs-lookup"><span data-stu-id="4d42c-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="4d42c-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="4d42c-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="4d42c-132">[in] Masque de bits d’indicateurs copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4d42c-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="4d42c-133">Les indicateurs fournissent des informations sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="4d42c-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="4d42c-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="4d42c-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="4d42c-135">[in] Masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4d42c-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="4d42c-136">Ces indicateurs fournissent davantage d’informations sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="4d42c-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="4d42c-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="4d42c-137">_ulAccess_</span></span>
  
> <span data-ttu-id="4d42c-138">[in] Indicateur qui indique le niveau d’autorisation pour le message qui s’affiche dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d42c-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="4d42c-139">Ces informations sont copiées à partir de la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4d42c-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="4d42c-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="4d42c-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="4d42c-141">[in] Pointeur vers la classe de message de message affiché dans le formulaire, copié à partir de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="4d42c-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d42c-142">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4d42c-142">Return value</span></span>

<span data-ttu-id="4d42c-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d42c-143">S_OK</span></span> 
  
> <span data-ttu-id="4d42c-144">Le formulaire est affiché avec succès.</span><span class="sxs-lookup"><span data-stu-id="4d42c-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="4d42c-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4d42c-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4d42c-146">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4d42c-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4d42c-147">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d42c-147">Remarks</span></span>

<span data-ttu-id="4d42c-148">La méthode **IMAPISession::ShowForm** affiche un formulaire de message qui a été préparé par la méthode **IMAPISession::PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="4d42c-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d42c-149">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="4d42c-149">Notes to callers</span></span>

<span data-ttu-id="4d42c-150">Vous devez disposer d’une seule référence au message passé dans _lpMessage_ paramètre la méthode **PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="4d42c-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="4d42c-151">Sachez que les implémentations de formulaire peuvent renvoyer des valeurs d’erreur autres que ceux documentés par MAPI.</span><span class="sxs-lookup"><span data-stu-id="4d42c-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="4d42c-152">Si vous pouvez utiliser ces valeurs d’erreur pour déterminer plus précise de la condition d’erreur, faites-le.</span><span class="sxs-lookup"><span data-stu-id="4d42c-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="4d42c-153">Dans le cas contraire, gérer ces erreurs comme vous le feriez MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="4d42c-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4d42c-154">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4d42c-154">MFCMAPI reference</span></span>

<span data-ttu-id="4d42c-155">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4d42c-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4d42c-156">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4d42c-156">**File**</span></span>|<span data-ttu-id="4d42c-157">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4d42c-157">**Function**</span></span>|<span data-ttu-id="4d42c-158">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4d42c-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d42c-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4d42c-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4d42c-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="4d42c-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="4d42c-161">MFCMAPI utilise la méthode **IMAPISession::ShowForm** , avec la méthode **PrepareForm** , pour afficher un message dans un formulaire modal.</span><span class="sxs-lookup"><span data-stu-id="4d42c-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d42c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d42c-162">See also</span></span>



[<span data-ttu-id="4d42c-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4d42c-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="4d42c-164">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4d42c-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="4d42c-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4d42c-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="4d42c-166">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d42c-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="4d42c-167">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4d42c-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

