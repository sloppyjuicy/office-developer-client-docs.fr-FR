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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783843"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="a6ad6-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="a6ad6-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="a6ad6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6ad6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6ad6-105">Déplace le message en cours dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="a6ad6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6ad6-106">Parameters</span></span>

 <span data-ttu-id="a6ad6-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="a6ad6-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="a6ad6-108">[in] Pointeur vers le dossier dans lequel le message doit être déplacé.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="a6ad6-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="a6ad6-109">_pViewContext_</span></span>
  
> <span data-ttu-id="a6ad6-110">[in] Pointeur vers un objet de contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="a6ad6-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="a6ad6-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="a6ad6-112">[in] Pointeur vers une structure [RECT](http://msdn.microsoft.com/fr-fr/library/dd162897%28VS.85%29.aspx) qui contient la taille de la fenêtre et la position du formulaire actif.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-112">[in] A pointer to a [RECT](http://msdn.microsoft.com/fr-fr/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="a6ad6-113">Le formulaire suivant utilise également ce rectangle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a6ad6-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a6ad6-114">Return value</span></span>

<span data-ttu-id="a6ad6-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6ad6-115">S_OK</span></span> 
  
> <span data-ttu-id="a6ad6-116">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a6ad6-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a6ad6-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a6ad6-118">L’opération n’est pas pris en charge par ce site de message.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6ad6-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6ad6-119">Remarks</span></span>

<span data-ttu-id="a6ad6-120">Objets de formulaire appeler la méthode **IMAPIMessageSite::MoveMessage** pour déplacer le message en cours vers un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6ad6-121">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a6ad6-121">Notes to implementers</span></span>

<span data-ttu-id="a6ad6-122">Implémentation de l’utilisateur du formulaire de **MoveMessage** doit appeler la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , en passant l’indicateur VCDIR_MOVE, avant de déplacer réellement le message vers un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="a6ad6-123">Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction Windows [GetWindowRect](http://msdn.microsoft.com/fr-fr/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="a6ad6-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/fr-fr/library/ms633519) function.</span></span> 
  
<span data-ttu-id="a6ad6-124">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a6ad6-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6ad6-125">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="a6ad6-125">Notes to callers</span></span>

<span data-ttu-id="a6ad6-126">Après le renvoi de **MoveMessage**, formulaires doivent vérifier pour un message en cours et se fermer puis si aucune n’existe.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a6ad6-127">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a6ad6-127">MFCMAPI reference</span></span>

<span data-ttu-id="a6ad6-128">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a6ad6-129">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a6ad6-129">**File**</span></span>|<span data-ttu-id="a6ad6-130">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a6ad6-130">**Function**</span></span>|<span data-ttu-id="a6ad6-131">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a6ad6-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a6ad6-132">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a6ad6-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a6ad6-133">CMyMAPIFormViewer::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="a6ad6-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="a6ad6-134">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6ad6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6ad6-135">See also</span></span>



[<span data-ttu-id="a6ad6-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="a6ad6-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="a6ad6-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6ad6-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a6ad6-138">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a6ad6-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a6ad6-139">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="a6ad6-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

