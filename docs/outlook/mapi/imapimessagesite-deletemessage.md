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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783828"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="c9074-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="c9074-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="c9074-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9074-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9074-105">Supprime le message en cours.</span><span class="sxs-lookup"><span data-stu-id="c9074-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="c9074-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9074-106">Parameters</span></span>

 <span data-ttu-id="c9074-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="c9074-107">_pViewContext_</span></span>
  
> <span data-ttu-id="c9074-108">[in] Pointeur vers un objet de contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="c9074-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="c9074-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="c9074-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="c9074-110">[in] Pointeur vers une structure [RECT](http://msdn.microsoft.com/fr-fr/library/dd162897%28VS.85%29.aspx) qui contient la taille de la fenêtre et la position du formulaire actif.</span><span class="sxs-lookup"><span data-stu-id="c9074-110">[in] A pointer to a [RECT](http://msdn.microsoft.com/fr-fr/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="c9074-111">Le formulaire suivant utilise également ce rectangle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c9074-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9074-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c9074-112">Return value</span></span>

<span data-ttu-id="c9074-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9074-113">S_OK</span></span> 
  
> <span data-ttu-id="c9074-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c9074-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c9074-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c9074-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c9074-116">L’opération n’est pas pris en charge par ce site de message.</span><span class="sxs-lookup"><span data-stu-id="c9074-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9074-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9074-117">Remarks</span></span>

<span data-ttu-id="c9074-118">Un objet form appelle la méthode **IMAPIMessageSite::DeleteMessage** pour supprimer le message qui affiche le formulaire actuellement.</span><span class="sxs-lookup"><span data-stu-id="c9074-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9074-119">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c9074-119">Notes to callers</span></span>

<span data-ttu-id="c9074-120">Après le renvoi de **DeleteMessage**, objets de formulaire doivent vérifier un nouveau message et puis faire disparaître eux-mêmes si aucune n’existe.</span><span class="sxs-lookup"><span data-stu-id="c9074-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="c9074-121">Pour déterminer si le message effectuées **DeleteMessage** a été supprimé ou déplacé vers un dossier **Éléments supprimés** , un objet de formulaire peut appeler la méthode [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) pour déterminer si l’indicateur DELETE_IS_MOVE a été renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c9074-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c9074-122">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c9074-122">Notes to implementers</span></span>

<span data-ttu-id="c9074-123">Si l’implémentation d’une visionneuse formulaire de la méthode **DeleteMessage** déplace le message suivant après avoir supprimé un message, l’implémentation doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) et transmettez l’indicateur VCDIR_DELETE avant d’exécuter la suppression effective.</span><span class="sxs-lookup"><span data-stu-id="c9074-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="c9074-124">Si l’implémentation d’une visionneuse formulaire de **DeleteMessage** déplace le message supprimé (par exemple, pour un dossier **Éléments supprimés** ), l’implémentation doit enregistrer les modifications dans le message si le message a été modifié.</span><span class="sxs-lookup"><span data-stu-id="c9074-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="c9074-125">Une implémentation classique de **DeleteMessage** effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9074-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="c9074-126">Si l’implémentation est déplacé le message, il appelle la méthode [IPersistMessage::Save](ipersistmessage-save.md) , en passant **null** dans le paramètre _pMessage_ et **la valeur true** dans le paramètre _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="c9074-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="c9074-127">Il appelle la méthode **IMAPIViewContext::ActivateNext** , en passant l’indicateur VCDIR_DELETE dans le paramètre _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="c9074-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="c9074-128">Si l’appel **ActivateNext** échoue, elle renvoie.</span><span class="sxs-lookup"><span data-stu-id="c9074-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="c9074-129">Si **ActivateNext** renvoie S_FALSE, il appelle la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="c9074-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="c9074-130">Il supprime ou déplace le message.</span><span class="sxs-lookup"><span data-stu-id="c9074-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="c9074-131">Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction Windows [GetWindowRect](http://msdn.microsoft.com/fr-fr/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="c9074-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/fr-fr/library/ms633519) function.</span></span> 
  
<span data-ttu-id="c9074-132">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c9074-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c9074-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c9074-133">MFCMAPI reference</span></span>

<span data-ttu-id="c9074-134">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9074-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c9074-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c9074-135">**File**</span></span>|<span data-ttu-id="c9074-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c9074-136">**Function**</span></span>|<span data-ttu-id="c9074-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c9074-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9074-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c9074-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c9074-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="c9074-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="c9074-140">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="c9074-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9074-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9074-141">See also</span></span>



[<span data-ttu-id="c9074-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="c9074-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="c9074-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="c9074-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="c9074-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="c9074-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="c9074-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="c9074-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="c9074-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9074-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="c9074-147">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c9074-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c9074-148">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="c9074-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

