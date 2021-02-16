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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412526"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="a9398-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="a9398-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="a9398-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9398-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9398-105">Affiche un formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9398-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a9398-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9398-106">Parameters</span></span>

 <span data-ttu-id="a9398-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a9398-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a9398-108">[in] Poignée vers la fenêtre parent du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9398-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="a9398-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="a9398-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="a9398-110">[in] Pointeur vers la magasin de messages qui contient le dossier pointé par _le paramètre lpParentFolder._</span><span class="sxs-lookup"><span data-stu-id="a9398-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="a9398-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="a9398-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="a9398-112">[in] Pointeur vers le dossier dans lequel le message associé au paramètre  _ulMessageToken_ a été créé.</span><span class="sxs-lookup"><span data-stu-id="a9398-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="a9398-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a9398-113">_lpInterface_</span></span>
  
> <span data-ttu-id="a9398-114">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message affiché dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9398-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="a9398-115">Le  _paramètre lpInterface_ doit être NULL ou IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="a9398-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="a9398-116">La transmission DE NULL entraîne l’utilisation [de l’interface standard, IMessage.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="a9398-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="a9398-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="a9398-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="a9398-118">[in] Jeton associé au message à afficher dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9398-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="a9398-119">Le  _paramètre ulMessageToken_ doit être paramétré sur le contenu du paramètre  _lpulMessageToken_ de l’appel précédent à [IMAPISession::P repareForm](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="a9398-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="a9398-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="a9398-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="a9398-121">[in] Réservé ; doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="a9398-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="a9398-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9398-122">_ulFlags_</span></span>
  
> <span data-ttu-id="a9398-123">[in] Masque de bits d’indicateurs qui contrôle comment et si le message est enregistré.</span><span class="sxs-lookup"><span data-stu-id="a9398-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="a9398-124">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="a9398-124">The following flags can be set:</span></span>
    
<span data-ttu-id="a9398-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a9398-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="a9398-126">Le message n’a jamais été enregistré (autrement dit, sa méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) n’a jamais été appelée).</span><span class="sxs-lookup"><span data-stu-id="a9398-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="a9398-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a9398-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="a9398-128">Le message doit être enregistré dans son dossier parent.</span><span class="sxs-lookup"><span data-stu-id="a9398-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="a9398-129">Le message n’est pas traitée pour l’envoi, mais publiée dans le dossier à la place.</span><span class="sxs-lookup"><span data-stu-id="a9398-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="a9398-130">Si cet indicateur n’est pas définie, le message est copié dans la boîte d’envoi et est traitée pour l’envoi.</span><span class="sxs-lookup"><span data-stu-id="a9398-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="a9398-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="a9398-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="a9398-132">[in] Masque de bits d’indicateurs copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="a9398-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="a9398-133">Les indicateurs fournissent des informations sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="a9398-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="a9398-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="a9398-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="a9398-135">[in] Masque de bits d’indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="a9398-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="a9398-136">Ces indicateurs fournissent des informations supplémentaires sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="a9398-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="a9398-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="a9398-137">_ulAccess_</span></span>
  
> <span data-ttu-id="a9398-138">[in] Indicateur qui indique le niveau d’autorisation pour le message affiché dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9398-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="a9398-139">Ces informations sont copiées à partir **de la propriété PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="a9398-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="a9398-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a9398-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="a9398-141">[in] Pointeur vers la classe de message du message affiché dans le formulaire, copié à partir de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="a9398-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a9398-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9398-142">Return value</span></span>

<span data-ttu-id="a9398-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9398-143">S_OK</span></span> 
  
> <span data-ttu-id="a9398-144">Le formulaire a été affiché avec succès.</span><span class="sxs-lookup"><span data-stu-id="a9398-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="a9398-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a9398-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a9398-146">L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a9398-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a9398-147">Remarques</span><span class="sxs-lookup"><span data-stu-id="a9398-147">Remarks</span></span>

<span data-ttu-id="a9398-148">La **méthode IMAPISession::ShowForm** affiche un formulaire de message qui a été préparé par la méthode **IMAPISession::P repareForm.**</span><span class="sxs-lookup"><span data-stu-id="a9398-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a9398-149">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="a9398-149">Notes to callers</span></span>

<span data-ttu-id="a9398-150">Vous ne devez avoir qu’une seule référence au message transmis dans le paramètre _lpMessage_ de la méthode **PrepareForm.**</span><span class="sxs-lookup"><span data-stu-id="a9398-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="a9398-151">N’ignorez pas que les implémentations de formulaire peuvent renvoyer des valeurs d’erreur autres que celles documentées par MAPI.</span><span class="sxs-lookup"><span data-stu-id="a9398-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="a9398-152">Si vous pouvez utiliser ces valeurs d’erreur pour déterminer plus précisément la condition d’erreur, faites-le.</span><span class="sxs-lookup"><span data-stu-id="a9398-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="a9398-153">Sinon, traitez ces erreurs comme vous le feriez pour MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a9398-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a9398-154">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a9398-154">MFCMAPI reference</span></span>

<span data-ttu-id="a9398-155">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a9398-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a9398-156">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a9398-156">**File**</span></span>|<span data-ttu-id="a9398-157">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a9398-157">**Function**</span></span>|<span data-ttu-id="a9398-158">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a9398-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a9398-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a9398-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a9398-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="a9398-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="a9398-161">MFCMAPI utilise la méthode **IMAPISession::ShowForm,** ainsi que la méthode **PrepareForm,** pour afficher un message sous forme modale.</span><span class="sxs-lookup"><span data-stu-id="a9398-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9398-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9398-162">See also</span></span>



[<span data-ttu-id="a9398-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a9398-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a9398-164">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a9398-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="a9398-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a9398-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="a9398-166">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9398-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a9398-167">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a9398-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

