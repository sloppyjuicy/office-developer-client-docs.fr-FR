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
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321412"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="cae02-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="cae02-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="cae02-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cae02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cae02-105">Supprime le message actif.</span><span class="sxs-lookup"><span data-stu-id="cae02-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="cae02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cae02-106">Parameters</span></span>

 <span data-ttu-id="cae02-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="cae02-107">_pViewContext_</span></span>
  
> <span data-ttu-id="cae02-108">dans Pointeur vers un objet de contexte d'affichage.</span><span class="sxs-lookup"><span data-stu-id="cae02-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="cae02-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="cae02-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="cae02-110">dans Pointeur vers une structure [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) qui contient la position et la taille de la fenêtre du formulaire actif.</span><span class="sxs-lookup"><span data-stu-id="cae02-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="cae02-111">Le formulaire suivant affiché utilise également le rectangle de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cae02-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cae02-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cae02-112">Return value</span></span>

<span data-ttu-id="cae02-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="cae02-113">S_OK</span></span> 
  
> <span data-ttu-id="cae02-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="cae02-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cae02-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cae02-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cae02-116">L'opération n'est pas prise en charge par ce site de messages.</span><span class="sxs-lookup"><span data-stu-id="cae02-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cae02-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="cae02-117">Remarks</span></span>

<span data-ttu-id="cae02-118">Un objet Form appelle la méthode **IMAPIMessageSite::D eletemessage** pour supprimer le message actuellement affiché par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="cae02-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cae02-119">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="cae02-119">Notes to callers</span></span>

<span data-ttu-id="cae02-120">Suite au retour de **DeleteMessage**, les objets de formulaire doivent vérifier la présence d'un nouveau message, puis le faire disparaître s'il n'en existe pas.</span><span class="sxs-lookup"><span data-stu-id="cae02-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="cae02-121">Pour déterminer si le message **DeleteMessage** a été supprimé ou déplacé vers un dossier **éléments supprimés** , un objet Form peut appeler la méthode [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) afin de déterminer si l'indicateur DELETE_IS_MOVE a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="cae02-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cae02-122">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="cae02-122">Notes to implementers</span></span>

<span data-ttu-id="cae02-123">Si l'implémentation d'une visionneuse de formulaires de la méthode **DeleteMessage** passe au message suivant une fois qu'il a supprimé un message, l'implémentation doit appeler la méthode [IMAPIViewContext:: ActivateNext,](imapiviewcontext-activatenext.md) et passer l'indicateur VCDIR_DELETE avant d'effectuer la suppression effective.</span><span class="sxs-lookup"><span data-stu-id="cae02-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="cae02-124">Si l'implémentation d'une visionneuse de formulaires de **DeleteMessage** déplace le message supprimé (par exemple, vers un dossier **éléments supprimés** ), l'implémentation doit enregistrer les modifications apportées au message si celui-ci a été modifié.</span><span class="sxs-lookup"><span data-stu-id="cae02-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="cae02-125">Une implémentation type de **DeleteMessage** effectue les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="cae02-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="cae02-126">Si l'implémentation déplace le message, elle appelle la méthode [IPersistMessage:: Save](ipersistmessage-save.md) , en transmettant **null** dans le paramètre _pMessage_ et **true** dans le paramètre _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="cae02-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="cae02-127">Il appelle la méthode **IMAPIViewContext:: ActivateNext,** , en transmettant l'indicateur VCDIR_DELETE dans le paramètre _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="cae02-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="cae02-128">Si l'appel **ActivateNext,** échoue, il renvoie.</span><span class="sxs-lookup"><span data-stu-id="cae02-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="cae02-129">Si **ActivateNext,** renvoie S_FALSE, il appelle la méthode [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="cae02-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="cae02-130">Il supprime ou déplace le message.</span><span class="sxs-lookup"><span data-stu-id="cae02-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="cae02-131">Pour obtenir la structure **Rect** utilisée par la fenêtre d'un formulaire, appelez la fonction [GetWindowRect](https://msdn.microsoft.com/library/ms633519) de Windows.</span><span class="sxs-lookup"><span data-stu-id="cae02-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="cae02-132">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="cae02-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cae02-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cae02-133">MFCMAPI reference</span></span>

<span data-ttu-id="cae02-134">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cae02-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cae02-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="cae02-135">**File**</span></span>|<span data-ttu-id="cae02-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="cae02-136">**Function**</span></span>|<span data-ttu-id="cae02-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="cae02-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cae02-138">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="cae02-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="cae02-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="cae02-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="cae02-140">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="cae02-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cae02-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cae02-141">See also</span></span>



[<span data-ttu-id="cae02-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="cae02-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="cae02-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="cae02-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="cae02-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="cae02-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="cae02-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="cae02-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="cae02-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cae02-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="cae02-147">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="cae02-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="cae02-148">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="cae02-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

