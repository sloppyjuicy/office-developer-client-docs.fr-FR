---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396490"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="d0dd3-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="d0dd3-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="d0dd3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0dd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0dd3-105">Supprime le message en cours.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="d0dd3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0dd3-106">Parameters</span></span>

 <span data-ttu-id="d0dd3-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="d0dd3-107">_pViewContext_</span></span>
  
> <span data-ttu-id="d0dd3-108">[in] Pointeur vers un objet de contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="d0dd3-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="d0dd3-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="d0dd3-110">[in] Pointeur vers une structure [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) qui contient la taille de la fenêtre et la position du formulaire actif.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="d0dd3-111">Le formulaire suivant utilise également ce rectangle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d0dd3-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0dd3-112">Return value</span></span>

<span data-ttu-id="d0dd3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0dd3-113">S_OK</span></span> 
  
> <span data-ttu-id="d0dd3-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d0dd3-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d0dd3-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d0dd3-116">L’opération n’est pas pris en charge par ce site de message.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0dd3-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0dd3-117">Remarks</span></span>

<span data-ttu-id="d0dd3-118">Un objet form appelle la méthode **IMAPIMessageSite::DeleteMessage** pour supprimer le message qui affiche le formulaire actuellement.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d0dd3-119">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="d0dd3-119">Notes to callers</span></span>

<span data-ttu-id="d0dd3-120">Après le renvoi de **DeleteMessage**, objets de formulaire doivent vérifier un nouveau message et puis faire disparaître eux-mêmes si aucune n’existe.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="d0dd3-121">Pour déterminer si le message effectuées **DeleteMessage** a été supprimé ou déplacé vers un dossier **Éléments supprimés** , un objet de formulaire peut appeler la méthode [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) pour déterminer si l’indicateur DELETE_IS_MOVE a été renvoyée.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d0dd3-122">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="d0dd3-122">Notes to implementers</span></span>

<span data-ttu-id="d0dd3-123">Si l’implémentation d’une visionneuse formulaire de la méthode **DeleteMessage** déplace le message suivant après avoir supprimé un message, l’implémentation doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) et transmettez l’indicateur VCDIR_DELETE avant d’exécuter la suppression effective.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="d0dd3-124">Si l’implémentation d’une visionneuse formulaire de **DeleteMessage** déplace le message supprimé (par exemple, pour un dossier **Éléments supprimés** ), l’implémentation doit enregistrer les modifications dans le message si le message a été modifié.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="d0dd3-125">Une implémentation classique de **DeleteMessage** effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0dd3-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="d0dd3-126">Si l’implémentation est déplacé le message, il appelle la méthode [IPersistMessage::Save](ipersistmessage-save.md) , en passant **null** dans le paramètre _pMessage_ et **la valeur true** dans le paramètre _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="d0dd3-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="d0dd3-127">Il appelle la méthode **IMAPIViewContext::ActivateNext** , en passant l’indicateur VCDIR_DELETE dans le paramètre _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="d0dd3-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="d0dd3-128">Si l’appel **ActivateNext** échoue, elle renvoie.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="d0dd3-129">Si **ActivateNext** renvoie S_FALSE, il appelle la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="d0dd3-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="d0dd3-130">Il supprime ou déplace le message.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="d0dd3-131">Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="d0dd3-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="d0dd3-132">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d0dd3-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d0dd3-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d0dd3-133">MFCMAPI reference</span></span>

<span data-ttu-id="d0dd3-134">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d0dd3-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d0dd3-135">**File**</span></span>|<span data-ttu-id="d0dd3-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d0dd3-136">**Function**</span></span>|<span data-ttu-id="d0dd3-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d0dd3-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0dd3-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d0dd3-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d0dd3-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="d0dd3-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="d0dd3-140">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="d0dd3-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0dd3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0dd3-141">See also</span></span>



[<span data-ttu-id="d0dd3-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d0dd3-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="d0dd3-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d0dd3-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="d0dd3-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="d0dd3-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="d0dd3-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="d0dd3-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="d0dd3-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0dd3-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d0dd3-147">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="d0dd3-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d0dd3-148">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="d0dd3-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

