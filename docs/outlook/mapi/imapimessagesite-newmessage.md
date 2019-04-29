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
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438770"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="4861d-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="4861d-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="4861d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4861d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4861d-105">Crée un message.</span><span class="sxs-lookup"><span data-stu-id="4861d-105">Creates a new message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4861d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4861d-106">Parameters</span></span>

 <span data-ttu-id="4861d-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="4861d-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="4861d-108">dans Indique dans quel dossier le message doit être composé.</span><span class="sxs-lookup"><span data-stu-id="4861d-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="4861d-109">Si la variable a la valeur FALSe, le paramètre _pFolderFocus_ est ignoré et la visionneuse de formulaires peut composer le message dans n'importe quel dossier.</span><span class="sxs-lookup"><span data-stu-id="4861d-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="4861d-110">Si la variable a la valeur TRUE et si NULL est transmis dans le paramètre _pFolderFocus_ , le message est composé dans le dossier actif.</span><span class="sxs-lookup"><span data-stu-id="4861d-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="4861d-111">Si la variable est TRUE et qu'une valeur non NULL est transmise dans _pFolderFocus_, le message est composé dans le dossier désigné par _pFolderFocus_.</span><span class="sxs-lookup"><span data-stu-id="4861d-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="4861d-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="4861d-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="4861d-113">dans Pointeur vers le dossier où le nouveau message est créé.</span><span class="sxs-lookup"><span data-stu-id="4861d-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="4861d-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="4861d-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="4861d-115">dans Pointeur vers l'objet de formulaire pour le nouveau formulaire.</span><span class="sxs-lookup"><span data-stu-id="4861d-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="4861d-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="4861d-116">_ppMessage_</span></span>
  
> <span data-ttu-id="4861d-117">remarquer Pointeur vers un pointeur vers le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4861d-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="4861d-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="4861d-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="4861d-119">remarquer Pointeur vers un pointeur vers un objet de site de message pour le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4861d-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="4861d-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="4861d-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="4861d-121">remarquer Pointeur vers un pointeur vers un contexte d'affichage qui est approprié pour passer à un nouveau formulaire avec le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4861d-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="4861d-122">Si le formulaire implémente son propre contexte d'affichage, la valeur NULL peut être transmise au paramètre _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="4861d-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4861d-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4861d-123">Return value</span></span>

<span data-ttu-id="4861d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="4861d-124">S_OK</span></span> 
  
> <span data-ttu-id="4861d-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4861d-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4861d-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="4861d-126">Remarks</span></span>

<span data-ttu-id="4861d-127">Les objets de formulaire appellent la méthode **IMAPIMessageSite:: newMessage,** pour créer un message.</span><span class="sxs-lookup"><span data-stu-id="4861d-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="4861d-128">Le formulaire utilise **newMessage,** pour obtenir un nouveau message et le site de messages associé à partir de sa vue.</span><span class="sxs-lookup"><span data-stu-id="4861d-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="4861d-129">Il peut ensuite modifier le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4861d-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="4861d-130">Vous pouvez également obtenir un contexte de vue associé en transmettant une valeur non NULL dans le paramètre _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="4861d-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="4861d-131">Ce contexte d'affichage peut être utilisé directement, ou il peut être regroupé et transmis au nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4861d-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="4861d-132">Si une implémentation complète est requise, transmettez la valeur NULL dans _ppViewContext_.</span><span class="sxs-lookup"><span data-stu-id="4861d-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="4861d-133">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="4861d-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4861d-134">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4861d-134">MFCMAPI reference</span></span>

<span data-ttu-id="4861d-135">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4861d-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4861d-136">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4861d-136">**File**</span></span>|<span data-ttu-id="4861d-137">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4861d-137">**Function**</span></span>|<span data-ttu-id="4861d-138">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4861d-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4861d-139">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="4861d-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="4861d-140">CMyMAPIFormViewer:: newMessage,</span><span class="sxs-lookup"><span data-stu-id="4861d-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="4861d-141">MFCMAPI utilise la méthode **IMAPIMessageSite:: newMessage,** pour créer un nouveau message, instancier une nouvelle visionneuse de formulaires et appeler **SetPersist** pour définir le message dans la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="4861d-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="4861d-142">Enfin, il renvoie la visionneuse de formulaires en tant que site de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4861d-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4861d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4861d-143">See also</span></span>



[<span data-ttu-id="4861d-144">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4861d-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="4861d-145">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4861d-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="4861d-146">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4861d-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4861d-147">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="4861d-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

