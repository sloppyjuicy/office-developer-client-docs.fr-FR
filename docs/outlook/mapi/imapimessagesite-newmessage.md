---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 133a2ae3896b9aaedb502cb77516040c53584882
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563736"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="68766-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="68766-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="68766-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68766-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68766-105">Crée un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="68766-105">Creates a new message.</span></span>
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="68766-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68766-106">Parameters</span></span>

 <span data-ttu-id="68766-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="68766-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="68766-108">[in] Indique le dossier dans lequel le message doit être composé.</span><span class="sxs-lookup"><span data-stu-id="68766-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="68766-109">Si la variable a la valeur FALSE, le paramètre _pFolderFocus_ est ignoré et la visionneuse de formulaire permettre composer le message dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="68766-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="68766-110">Si la variable a la valeur TRUE et NULL est passé dans le paramètre _pFolderFocus_ , le message est composé dans le dossier actif.</span><span class="sxs-lookup"><span data-stu-id="68766-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="68766-111">Si la variable a la valeur TRUE et une valeur non nulle est passée _pFolderFocus_, le message se compose dans le dossier désigné par _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="68766-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="68766-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="68766-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="68766-113">[in] Pointeur vers le dossier dans lequel le nouveau message est créé.</span><span class="sxs-lookup"><span data-stu-id="68766-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="68766-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="68766-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="68766-115">[in] Pointeur vers l’objet de formulaire pour le nouveau formulaire.</span><span class="sxs-lookup"><span data-stu-id="68766-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="68766-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="68766-116">_ppMessage_</span></span>
  
> <span data-ttu-id="68766-117">[out] Pointeur vers un pointeur vers le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="68766-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="68766-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="68766-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="68766-119">[out] Pointeur vers un pointeur vers un objet de site de message du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="68766-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="68766-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="68766-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="68766-121">[out] Pointeur vers un pointeur vers un contexte de vue est approprié pour passer à un nouveau formulaire avec le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="68766-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="68766-122">Si le formulaire implémente son propre contexte de vue, NULL peut être passé dans le paramètre _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="68766-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68766-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="68766-123">Return value</span></span>

<span data-ttu-id="68766-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="68766-124">S_OK</span></span> 
  
> <span data-ttu-id="68766-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="68766-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68766-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="68766-126">Remarks</span></span>

<span data-ttu-id="68766-127">Objets de formulaire appeler la méthode **IMAPIMessageSite::NewMessage** pour créer un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="68766-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="68766-128">Le formulaire utilise **NewMessage** pour obtenir un nouveau message et le site de message associé à partir de son affichage.</span><span class="sxs-lookup"><span data-stu-id="68766-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="68766-129">Il peut ensuite modifier le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="68766-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="68766-130">Vous pouvez également obtenir un contexte de la vue associée en transmettant une valeur non NULL dans le paramètre _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="68766-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="68766-131">Ce contexte de vue peut être utilisé directement, ou pouvant être regroupé et transmis vers le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="68766-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="68766-132">Si une implémentation complète est requise, passez la valeur NULL dans _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="68766-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="68766-133">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="68766-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="68766-134">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="68766-134">MFCMAPI reference</span></span>

<span data-ttu-id="68766-135">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="68766-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="68766-136">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="68766-136">**File**</span></span>|<span data-ttu-id="68766-137">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="68766-137">**Function**</span></span>|<span data-ttu-id="68766-138">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="68766-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68766-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="68766-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="68766-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="68766-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="68766-141">MFCMAPI utilise la méthode **IMAPIMessageSite::NewMessage** pour créer un nouveau message, instanciez un nouvel Observateur de formulaire et appeler **SetPersist** pour définir le message de la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="68766-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="68766-142">Enfin, elle renvoie la visionneuse de formulaire en tant que le site de message.</span><span class="sxs-lookup"><span data-stu-id="68766-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68766-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68766-143">See also</span></span>



[<span data-ttu-id="68766-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68766-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="68766-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68766-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="68766-146">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="68766-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="68766-147">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="68766-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

