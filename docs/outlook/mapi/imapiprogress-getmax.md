---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436201"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="b071c-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="b071c-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="b071c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b071c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b071c-105">Renvoie le nombre maximal d'éléments dans l'opération pour afficher les informations d'avancement.</span><span class="sxs-lookup"><span data-stu-id="b071c-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="b071c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b071c-106">Parameters</span></span>

 <span data-ttu-id="b071c-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="b071c-107">_lpulMax_</span></span>
  
> <span data-ttu-id="b071c-108">remarquer Pointeur vers le nombre maximal d'éléments dans l'opération.</span><span class="sxs-lookup"><span data-stu-id="b071c-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b071c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b071c-109">Return value</span></span>

<span data-ttu-id="b071c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b071c-110">S_OK</span></span> 
  
> <span data-ttu-id="b071c-111">Le nombre maximal d'éléments dans l'opération a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="b071c-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b071c-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="b071c-112">Remarks</span></span>

<span data-ttu-id="b071c-113">La valeur maximale représente la fin de l'opération sous forme numérique.</span><span class="sxs-lookup"><span data-stu-id="b071c-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="b071c-114">La valeur peut être une valeur maximale globale, utilisée pour représenter l’étendue de l’intégralité de l’affichage de la progression, ou une valeur locale, utilisée pour représenter uniquement une partie de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b071c-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="b071c-115">La valeur du paramètre flag détermine si l'objet Progress reconnaît la valeur maximale comme étant locale ou globale.</span><span class="sxs-lookup"><span data-stu-id="b071c-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="b071c-116">Lorsque l'indicateur MAPI_TOP_LEVEL est défini, la valeur maximale est considérée comme étant globale et utilisée pour calculer l'avancement de l'opération entière.</span><span class="sxs-lookup"><span data-stu-id="b071c-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="b071c-117">Lorsque MAPI_TOP_LEVEL n'est pas défini, la valeur maximale est considérée comme étant locale, et les fournisseurs l'utilisent en interne pour afficher la progression des sous-objets de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="b071c-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="b071c-118">Les objets Progress enregistrent la valeur maximale locale uniquement pour le renvoyer à un fournisseur par le biais d'un appel **GetMax** .</span><span class="sxs-lookup"><span data-stu-id="b071c-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="b071c-119">Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b071c-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b071c-120">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b071c-120">Notes to implementers</span></span>

<span data-ttu-id="b071c-121">Initialisez la valeur maximale sur 1000.</span><span class="sxs-lookup"><span data-stu-id="b071c-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="b071c-122">Les fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md).</span><span class="sxs-lookup"><span data-stu-id="b071c-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="b071c-123">Pour plus d'informations sur la façon d'implémenter **GetMax** et les autres méthodes [méthode imapiprogress](imapiprogressiunknown.md) , consultez la rubrique [implémentation d'un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b071c-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b071c-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b071c-124">MFCMAPI reference</span></span>

<span data-ttu-id="b071c-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b071c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b071c-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b071c-126">**File**</span></span>|<span data-ttu-id="b071c-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b071c-127">**Function**</span></span>|<span data-ttu-id="b071c-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b071c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b071c-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="b071c-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="b071c-130">CMAPIProgress:: GetMax</span><span class="sxs-lookup"><span data-stu-id="b071c-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="b071c-131">MFCMAPI utilise la méthode **méthode imapiprogress:: GetMax** pour obtenir la valeur maximale de l'objet Progress.</span><span class="sxs-lookup"><span data-stu-id="b071c-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="b071c-132">Renvoie 1000 sauf si les limites ont été définies précédemment à l'aide de la méthode **méthode imapiprogress:: SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="b071c-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b071c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b071c-133">See also</span></span>



[<span data-ttu-id="b071c-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="b071c-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="b071c-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="b071c-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="b071c-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="b071c-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="b071c-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b071c-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="b071c-138">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="b071c-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b071c-139">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="b071c-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="b071c-140">Implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="b071c-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

