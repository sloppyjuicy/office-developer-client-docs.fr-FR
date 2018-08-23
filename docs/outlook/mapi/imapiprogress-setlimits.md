---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 010f69b70324d4280a34d2fe06d670e07d922d86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586773"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="4119b-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4119b-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="4119b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4119b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4119b-105">Définit les limites supérieures et inférieures pour le nombre d’éléments dans l’opération et des indicateurs qui déterminent comment les informations d’avancement sont calculées pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="4119b-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4119b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4119b-106">Parameters</span></span>

 <span data-ttu-id="4119b-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="4119b-107">_lpulMin_</span></span>
  
> <span data-ttu-id="4119b-108">[in] Pointeur vers une variable qui contient la limite inférieure d’éléments dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="4119b-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="4119b-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="4119b-109">_lpulMax_</span></span>
  
> <span data-ttu-id="4119b-110">[in] Pointeur vers une variable qui contient la limite supérieure d’éléments dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="4119b-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="4119b-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="4119b-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="4119b-112">[in] Masque de bits d’indicateurs qui contrôle le niveau de l’opération sur l’avancement des informations sont calculées.</span><span class="sxs-lookup"><span data-stu-id="4119b-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="4119b-113">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="4119b-113">The following flag can be set:</span></span>
    
<span data-ttu-id="4119b-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="4119b-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="4119b-115">Utilise les valeurs de paramètres de la méthode [IMAPIProgress::Progress](imapiprogress-progress.md) de _ulCount_ et _ulTotal_ , qui indiquent l’élément en cours de traitement et le nombre total d’éléments, respectivement, au cours d’incrémentation sur l’opération.</span><span class="sxs-lookup"><span data-stu-id="4119b-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="4119b-116">Lorsque cet indicateur est défini, les valeurs des limites inférieures et supérieures globales doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="4119b-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4119b-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4119b-117">Return value</span></span>

<span data-ttu-id="4119b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4119b-118">S_OK</span></span> 
  
> <span data-ttu-id="4119b-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4119b-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4119b-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4119b-120">Remarks</span></span>

<span data-ttu-id="4119b-121">Fournisseurs de services appeler la méthode **IMAPIProgress::SetLimits** pour définir ou effacer l’indicateur MAPI_TOP_LEVEL et définir les valeurs minimales et maximales globales et locales.</span><span class="sxs-lookup"><span data-stu-id="4119b-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="4119b-122">La valeur du paramètre indicateur affecte si l’objet de l’avancement comprend les valeurs minimales et maximales pour être local ou global.</span><span class="sxs-lookup"><span data-stu-id="4119b-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="4119b-123">Lorsque l’indicateur MAPI_TOP_LEVEL est défini, ces valeurs sont considérées comme globales et sont utilisés pour calculer l’avancement pour toute l’opération.</span><span class="sxs-lookup"><span data-stu-id="4119b-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="4119b-124">Objets de progression initialiser la valeur minimale globale à 1 et la valeur maximale globale et 1000.</span><span class="sxs-lookup"><span data-stu-id="4119b-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="4119b-125">Lorsque MAPI_TOP_LEVEL n’est pas définie, les valeurs minimales et maximales sont considérées comme locales et fournisseurs de les utilisent en interne pour afficher la progression de sous-objets de niveau inférieurs.</span><span class="sxs-lookup"><span data-stu-id="4119b-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="4119b-126">Objets de progression enregistrement les valeurs minimales et maximales locales uniquement afin qu’ils peuvent être renvoyées à fournisseurs lorsque les méthodes [IMAPIProgress::GetMin](imapiprogress-getmin.md) et [IMAPIProgress::GetMax](imapiprogress-getmax.md) sont appelées.</span><span class="sxs-lookup"><span data-stu-id="4119b-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="4119b-127">Pour plus d’informations sur l’implémentation des autres méthodes [IMAPIProgress](imapiprogressiunknown.md) et **SetLimits** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4119b-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="4119b-128">Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4119b-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4119b-129">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4119b-129">MFCMAPI reference</span></span>

<span data-ttu-id="4119b-130">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4119b-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4119b-131">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4119b-131">**File**</span></span>|<span data-ttu-id="4119b-132">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4119b-132">**Function**</span></span>|<span data-ttu-id="4119b-133">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4119b-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4119b-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="4119b-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="4119b-135">CMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4119b-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="4119b-136">MFCMAPI utilise la méthode **IMAPIProgress::SetLimits** pour définir les indicateurs pour l’objet de l’avancement des limites maximale et minimale.</span><span class="sxs-lookup"><span data-stu-id="4119b-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4119b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4119b-137">See also</span></span>



[<span data-ttu-id="4119b-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="4119b-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="4119b-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="4119b-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="4119b-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="4119b-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="4119b-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4119b-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="4119b-142">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4119b-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4119b-143">Afficher un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="4119b-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="4119b-144">Implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="4119b-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

