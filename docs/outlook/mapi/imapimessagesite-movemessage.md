---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321364"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="782e7-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="782e7-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="782e7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="782e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="782e7-105">Déplace le message actuel vers un dossier.</span><span class="sxs-lookup"><span data-stu-id="782e7-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="782e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="782e7-106">Parameters</span></span>

 <span data-ttu-id="782e7-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="782e7-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="782e7-108">[in] Pointeur vers le dossier dans lequel le message doit être déplacé.</span><span class="sxs-lookup"><span data-stu-id="782e7-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="782e7-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="782e7-109">_pViewContext_</span></span>
  
> <span data-ttu-id="782e7-110">[in] Pointeur vers un objet de contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="782e7-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="782e7-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="782e7-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="782e7-112">[in] Pointeur vers une structure [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) qui contient la taille et la position de la fenêtre du formulaire actuel.</span><span class="sxs-lookup"><span data-stu-id="782e7-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="782e7-113">Le formulaire suivant affiché utilise également ce rectangle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="782e7-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="782e7-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="782e7-114">Return value</span></span>

<span data-ttu-id="782e7-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="782e7-115">S_OK</span></span> 
  
> <span data-ttu-id="782e7-116">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="782e7-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="782e7-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="782e7-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="782e7-118">L’opération n’est pas prise en charge par ce site de message.</span><span class="sxs-lookup"><span data-stu-id="782e7-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="782e7-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="782e7-119">Remarks</span></span>

<span data-ttu-id="782e7-120">Les objets form appellent la méthode **IMAPIMessageSite::MoveMessage** pour déplacer le message actuel vers un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="782e7-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="782e7-121">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="782e7-121">Notes to implementers</span></span>

<span data-ttu-id="782e7-122">L’implémentation de **MoveMessage** d’une visionneuse de formulaire doit appeler la méthode [IMAPIViewContext::ActivateNext,](imapiviewcontext-activatenext.md) en passant l’indicateur VCDIR_MOVE, avant de déplacer réellement le message vers un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="782e7-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="782e7-123">Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction Windows [GetWindowRect.](https://msdn.microsoft.com/library/ms633519)</span><span class="sxs-lookup"><span data-stu-id="782e7-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="782e7-124">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="782e7-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="782e7-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="782e7-125">Notes to callers</span></span>

<span data-ttu-id="782e7-126">Après le renvoi de **MoveMessage,** les formulaires doivent vérifier la recherche d’un message actuel, puis se fermer s’il n’en existe aucun.</span><span class="sxs-lookup"><span data-stu-id="782e7-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="782e7-127">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="782e7-127">MFCMAPI reference</span></span>

<span data-ttu-id="782e7-128">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="782e7-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="782e7-129">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="782e7-129">**File**</span></span>|<span data-ttu-id="782e7-130">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="782e7-130">**Function**</span></span>|<span data-ttu-id="782e7-131">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="782e7-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="782e7-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="782e7-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="782e7-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="782e7-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="782e7-134">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="782e7-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="782e7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="782e7-135">See also</span></span>



[<span data-ttu-id="782e7-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="782e7-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="782e7-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="782e7-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="782e7-138">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="782e7-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="782e7-139">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="782e7-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

