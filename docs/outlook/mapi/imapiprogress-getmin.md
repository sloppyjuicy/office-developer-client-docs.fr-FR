---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783882"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="0d8e4-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="0d8e4-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="0d8e4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d8e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d8e4-105">Renvoie la valeur minimale dans la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) pour l’avancement des informations s’affichent.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="0d8e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d8e4-106">Parameters</span></span>

 <span data-ttu-id="0d8e4-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="0d8e4-107">_lpulMin_</span></span>
  
> <span data-ttu-id="0d8e4-108">[out] Pointeur vers le nombre minimal d’éléments dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d8e4-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0d8e4-109">Return value</span></span>

<span data-ttu-id="0d8e4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d8e4-110">S_OK</span></span> 
  
> <span data-ttu-id="0d8e4-111">Le nombre minimal d’éléments dans l’opération a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d8e4-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d8e4-112">Remarks</span></span>

<span data-ttu-id="0d8e4-113">La valeur minimale représente le début de l’opération sous forme numérique.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="0d8e4-114">La valeur peut être une valeur maximale globale, utilisé pour représenter l’étendue de l’affichage de la progression de l’intégralité ou une valeur locale, utilisé pour ne représenter qu’une partie de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="0d8e4-115">La valeur du paramètre indicateur affecte si l’objet de l’avancement comprend la valeur minimale pour être local ou global.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="0d8e4-116">Lorsque l’indicateur MAPI_TOP_LEVEL est défini, la valeur minimale est considéré comme étant global et est utilisée pour calculer l’avancement pour toute l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="0d8e4-117">Lorsque MAPI_TOP_LEVEL n’est pas définie, la valeur minimale est considérée comme étant locale et fournisseurs de l’utiliser en interne pour afficher la progression de sous-objets de niveau inférieurs.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="0d8e4-118">Objets de progression enregistrement la valeur minimale locale uniquement pour renvoyer à un fournisseur via un appel **GetMin** .</span><span class="sxs-lookup"><span data-stu-id="0d8e4-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0d8e4-119">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="0d8e4-119">Notes to implementers</span></span>

<span data-ttu-id="0d8e4-120">Initialiser la valeur minimale 1.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="0d8e4-121">Fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="0d8e4-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="0d8e4-122">Pour plus d’informations sur l’implémentation des autres méthodes [IMAPIProgress](imapiprogressiunknown.md) et **GetMin** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="0d8e4-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="0d8e4-123">Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="0d8e4-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0d8e4-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0d8e4-124">MFCMAPI reference</span></span>

<span data-ttu-id="0d8e4-125">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0d8e4-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0d8e4-126">**File**</span></span>|<span data-ttu-id="0d8e4-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="0d8e4-127">**Function**</span></span>|<span data-ttu-id="0d8e4-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="0d8e4-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d8e4-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="0d8e4-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="0d8e4-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="0d8e4-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="0d8e4-131">MFCMAPI utilise la méthode **IMAPIProgress::GetMin** pour obtenir la valeur minimale pour l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="0d8e4-132">Renvoie la valeur 1, sauf si la limite a été définie précédemment en appelant la méthode **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="0d8e4-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d8e4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d8e4-133">See also</span></span>



[<span data-ttu-id="0d8e4-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="0d8e4-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="0d8e4-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="0d8e4-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="0d8e4-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="0d8e4-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="0d8e4-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d8e4-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="0d8e4-138">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="0d8e4-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0d8e4-139">Afficher un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="0d8e4-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="0d8e4-140">L’implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="0d8e4-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

