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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421465"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="213fd-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="213fd-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="213fd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="213fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="213fd-105">Définit les limites inférieure et supérieure du nombre d'éléments dans l'opération, ainsi que les indicateurs qui contrôlent le mode de calcul des informations d'avancement pour l'opération.</span><span class="sxs-lookup"><span data-stu-id="213fd-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="213fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="213fd-106">Parameters</span></span>

 <span data-ttu-id="213fd-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="213fd-107">_lpulMin_</span></span>
  
> <span data-ttu-id="213fd-108">dans Pointeur vers une variable qui contient la limite inférieure des éléments de l'opération.</span><span class="sxs-lookup"><span data-stu-id="213fd-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="213fd-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="213fd-109">_lpulMax_</span></span>
  
> <span data-ttu-id="213fd-110">dans Pointeur vers une variable qui contient la limite supérieure des éléments de l'opération.</span><span class="sxs-lookup"><span data-stu-id="213fd-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="213fd-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="213fd-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="213fd-112">dans Masque de des indicateurs qui contrôle le niveau d'opération sur lequel les informations de progression sont calculées.</span><span class="sxs-lookup"><span data-stu-id="213fd-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="213fd-113">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="213fd-113">The following flag can be set:</span></span>
    
<span data-ttu-id="213fd-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="213fd-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="213fd-115">Utilise les valeurs des paramètres [méthode imapiprogress::P rogress](imapiprogress-progress.md) de la méthode _ulCount_ et _ulTotal_ , qui indiquent respectivement l'élément traité et le nombre total d'éléments pour incrémenter la progression de l'opération.</span><span class="sxs-lookup"><span data-stu-id="213fd-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="213fd-116">Lorsque cet indicateur est défini, les valeurs des limites inférieure et supérieure globales doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="213fd-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="213fd-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="213fd-117">Return value</span></span>

<span data-ttu-id="213fd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="213fd-118">S_OK</span></span> 
  
> <span data-ttu-id="213fd-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="213fd-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="213fd-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="213fd-120">Remarks</span></span>

<span data-ttu-id="213fd-121">Les fournisseurs de services appellent la méthode **méthode imapiprogress:: SetLimits** pour définir ou effacer l'indicateur MAPI_TOP_LEVEL et pour définir les valeurs minimales et maximales locales et globales.</span><span class="sxs-lookup"><span data-stu-id="213fd-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="213fd-122">La valeur du paramètre flag détermine si l'objet Progress comprend les valeurs minimale et maximale qui doivent être locales ou globales.</span><span class="sxs-lookup"><span data-stu-id="213fd-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="213fd-123">Lorsque l'indicateur MAPI_TOP_LEVEL est défini, ces valeurs sont considérées comme globales et sont utilisées pour calculer la progression de l'opération entière.</span><span class="sxs-lookup"><span data-stu-id="213fd-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="213fd-124">Les objets Progress initialisent la valeur minimale globale sur 1 et la valeur maximale globale sur 1000.</span><span class="sxs-lookup"><span data-stu-id="213fd-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="213fd-125">Lorsque MAPI_TOP_LEVEL n'est pas défini, les valeurs minimale et maximale sont considérées comme locales, et les fournisseurs les utilisent en interne pour afficher la progression des sous-objets de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="213fd-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="213fd-126">Les objets Progress enregistrent uniquement les valeurs minimales et maximales de sorte qu'ils puissent être renvoyés aux fournisseurs lorsque les méthodes [méthode imapiprogress:: GetMin](imapiprogress-getmin.md) et [méthode imapiprogress:: GetMax](imapiprogress-getmax.md) sont appelées.</span><span class="sxs-lookup"><span data-stu-id="213fd-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="213fd-127">Pour plus d'informations sur la façon d'implémenter **SetLimits** et les autres méthodes [méthode imapiprogress](imapiprogressiunknown.md) , consultez la rubrique [implémentation d'un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="213fd-128">Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="213fd-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="213fd-129">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="213fd-129">MFCMAPI reference</span></span>

<span data-ttu-id="213fd-130">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="213fd-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="213fd-131">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="213fd-131">**File**</span></span>|<span data-ttu-id="213fd-132">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="213fd-132">**Function**</span></span>|<span data-ttu-id="213fd-133">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="213fd-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="213fd-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="213fd-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="213fd-135">CMAPIProgress:: SetLimits</span><span class="sxs-lookup"><span data-stu-id="213fd-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="213fd-136">MFCMAPI utilise la méthode **méthode imapiprogress:: SetLimits** pour définir les limites et les indicateurs maximaux et minimaux de l'objet Progress.</span><span class="sxs-lookup"><span data-stu-id="213fd-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="213fd-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="213fd-137">See also</span></span>



[<span data-ttu-id="213fd-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="213fd-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="213fd-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="213fd-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="213fd-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="213fd-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="213fd-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="213fd-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="213fd-142">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="213fd-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="213fd-143">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="213fd-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="213fd-144">Implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="213fd-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

