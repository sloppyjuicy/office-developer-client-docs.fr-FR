---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329458"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="299d2-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="299d2-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="299d2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="299d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="299d2-105">Renvoie le contexte d'affichage actuel du formulaire.</span><span class="sxs-lookup"><span data-stu-id="299d2-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="299d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="299d2-106">Parameters</span></span>

 <span data-ttu-id="299d2-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="299d2-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="299d2-108">remarquer Pointeur vers un pointeur vers le contexte d'affichage du formulaire.</span><span class="sxs-lookup"><span data-stu-id="299d2-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="299d2-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="299d2-109">Return value</span></span>

<span data-ttu-id="299d2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="299d2-110">S_OK</span></span> 
  
> <span data-ttu-id="299d2-111">Le contexte d'affichage actuel du formulaire a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="299d2-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="299d2-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="299d2-112">S_FALSE</span></span> 
  
> <span data-ttu-id="299d2-113">Il n'existe pas de contexte d'affichage pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="299d2-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="299d2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="299d2-114">Remarks</span></span>

<span data-ttu-id="299d2-115">Les visionneuses de formulaires appellent **GetViewContext** pour obtenir un pointeur vers le contexte d'affichage établi dans un appel précédent à [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="299d2-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="299d2-116">Si aucun appel antérieur n'a été effectué vers **SetViewContext**, **GetViewContext** définit _ppViewContext_ sur null.</span><span class="sxs-lookup"><span data-stu-id="299d2-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="299d2-117">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="299d2-117">Notes to implementers</span></span>

<span data-ttu-id="299d2-118">Copiez le pointeur de contexte de vue de votre formulaire dans le pointeur transmis par la visionneuse de formulaire appelant dans le paramètre _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="299d2-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="299d2-119">Si le formulaire n'a pas de contexte d'affichage, affectez la valeur NULL à _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="299d2-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="299d2-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="299d2-120">MFCMAPI reference</span></span>

<span data-ttu-id="299d2-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="299d2-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="299d2-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="299d2-122">**File**</span></span>|<span data-ttu-id="299d2-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="299d2-123">**Function**</span></span>|<span data-ttu-id="299d2-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="299d2-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="299d2-125">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="299d2-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="299d2-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="299d2-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="299d2-127">MFCMAPI utilise la méthode **IMAPIForm:: GetViewContext** pour vérifier si un formulaire possède un contexte d'affichage.</span><span class="sxs-lookup"><span data-stu-id="299d2-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="299d2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="299d2-128">See also</span></span>



[<span data-ttu-id="299d2-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="299d2-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="299d2-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="299d2-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="299d2-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="299d2-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

