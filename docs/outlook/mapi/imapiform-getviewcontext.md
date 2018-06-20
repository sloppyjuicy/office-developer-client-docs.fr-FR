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
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783748"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="f6771-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="f6771-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="f6771-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6771-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6771-105">Renvoie le contexte actuel de la vue pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="f6771-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="f6771-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6771-106">Parameters</span></span>

 <span data-ttu-id="f6771-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="f6771-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="f6771-108">[out] Pointeur vers un pointeur vers le contexte de vue du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f6771-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f6771-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f6771-109">Return value</span></span>

<span data-ttu-id="f6771-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6771-110">S_OK</span></span> 
  
> <span data-ttu-id="f6771-111">Contexte d’affichage actuel du formulaire a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f6771-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="f6771-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f6771-112">S_FALSE</span></span> 
  
> <span data-ttu-id="f6771-113">Il n’existe aucun contexte de vue pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="f6771-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6771-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f6771-114">Remarks</span></span>

<span data-ttu-id="f6771-115">Visionneuses de formulaire appellent **GetViewContext** pour obtenir un pointeur vers le contexte de vue établi dans un appel précédent à [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="f6771-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="f6771-116">Si aucun appel précédent n’a été effectuée pour **SetViewContext**, **GetViewContext** définit _ppViewContext_ sur NULL.</span><span class="sxs-lookup"><span data-stu-id="f6771-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f6771-117">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f6771-117">Notes to implementers</span></span>

<span data-ttu-id="f6771-118">Copiez le pointeur de contexte de vue de votre formulaire dans le pointeur passé par la visionneuse de formulaire appelant dans le paramètre _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="f6771-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="f6771-119">Si le formulaire ne dispose pas d’un contexte de vue, _ppViewContext_ la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="f6771-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6771-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f6771-120">MFCMAPI reference</span></span>

<span data-ttu-id="f6771-121">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f6771-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6771-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f6771-122">**File**</span></span>|<span data-ttu-id="f6771-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f6771-123">**Function**</span></span>|<span data-ttu-id="f6771-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f6771-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6771-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f6771-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f6771-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="f6771-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="f6771-127">MFCMAPI utilise la méthode **IMAPIForm::GetViewContext** pour vérifier si un formulaire possède un contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="f6771-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6771-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6771-128">See also</span></span>



[<span data-ttu-id="f6771-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6771-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="f6771-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6771-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="f6771-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f6771-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

