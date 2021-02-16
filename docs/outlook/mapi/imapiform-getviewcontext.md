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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430902"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="923cf-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="923cf-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="923cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="923cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="923cf-105">Renvoie le contexte d’affichage actuel du formulaire.</span><span class="sxs-lookup"><span data-stu-id="923cf-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="923cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="923cf-106">Parameters</span></span>

 <span data-ttu-id="923cf-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="923cf-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="923cf-108">[out] Pointeur vers un pointeur vers le contexte d’affichage du formulaire.</span><span class="sxs-lookup"><span data-stu-id="923cf-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="923cf-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="923cf-109">Return value</span></span>

<span data-ttu-id="923cf-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="923cf-110">S_OK</span></span> 
  
> <span data-ttu-id="923cf-111">Le contexte d’affichage actuel du formulaire a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="923cf-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="923cf-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="923cf-112">S_FALSE</span></span> 
  
> <span data-ttu-id="923cf-113">Il n’existe aucun contexte d’affichage pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="923cf-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="923cf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="923cf-114">Remarks</span></span>

<span data-ttu-id="923cf-115">Les visionneuses de formulaire **appellent GetViewContext** pour obtenir un pointeur vers le contexte d’affichage établi dans un appel précédent à [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="923cf-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="923cf-116">Si aucun appel préalable n’a été effectué sur **SetViewContext**, **GetViewContext** définit  _ppViewContext_ sur NULL.</span><span class="sxs-lookup"><span data-stu-id="923cf-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="923cf-117">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="923cf-117">Notes to implementers</span></span>

<span data-ttu-id="923cf-118">Copiez le pointeur de contexte d’affichage de votre formulaire dans le pointeur transmis par la visionneuse de formulaire appelant dans le _paramètre ppViewContext._</span><span class="sxs-lookup"><span data-stu-id="923cf-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="923cf-119">Si le formulaire ne comporte pas de contexte d’affichage, définissez  _ppViewContext_ sur NULL.</span><span class="sxs-lookup"><span data-stu-id="923cf-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="923cf-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="923cf-120">MFCMAPI reference</span></span>

<span data-ttu-id="923cf-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="923cf-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="923cf-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="923cf-122">**File**</span></span>|<span data-ttu-id="923cf-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="923cf-123">**Function**</span></span>|<span data-ttu-id="923cf-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="923cf-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="923cf-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="923cf-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="923cf-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="923cf-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="923cf-127">MFCMAPI utilise la **méthode IMAPIForm::GetViewContext** pour vérifier si un formulaire possède un contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="923cf-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="923cf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="923cf-128">See also</span></span>



[<span data-ttu-id="923cf-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="923cf-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="923cf-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="923cf-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="923cf-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="923cf-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

