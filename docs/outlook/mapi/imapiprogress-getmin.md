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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6cd31f8ac713c21053db7ef461220a360ebeec74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404847"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="36459-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="36459-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="36459-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36459-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36459-105">Renvoie la valeur minimale dans la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) pour laquelle les informations de progression sont affichées.</span><span class="sxs-lookup"><span data-stu-id="36459-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="36459-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36459-106">Parameters</span></span>

 <span data-ttu-id="36459-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="36459-107">_lpulMin_</span></span>
  
> <span data-ttu-id="36459-108">[out] Pointeur vers le nombre minimal d’éléments dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="36459-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36459-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="36459-109">Return value</span></span>

<span data-ttu-id="36459-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="36459-110">S_OK</span></span> 
  
> <span data-ttu-id="36459-111">Le nombre minimal d’éléments dans l’opération a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="36459-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36459-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="36459-112">Remarks</span></span>

<span data-ttu-id="36459-113">La valeur minimale représente le début de l’opération au format numérique.</span><span class="sxs-lookup"><span data-stu-id="36459-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="36459-114">La valeur peut être une valeur maximale globale, utilisée pour représenter l’étendue de l’intégralité de l’affichage de la progression, ou une valeur locale, utilisée pour représenter uniquement une partie de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="36459-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="36459-115">La valeur du paramètre d’indicateur permet de déterminer si l’objet de progression considère la valeur minimale comme locale ou globale.</span><span class="sxs-lookup"><span data-stu-id="36459-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="36459-116">Lorsque l’indicateur MAPI_TOP_LEVEL est défini, la valeur minimale est globale et sert à calculer la progression pour l’intégralité de l’opération.</span><span class="sxs-lookup"><span data-stu-id="36459-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="36459-117">Si MAPI_TOP_LEVEL n’est pas défini, la valeur minimale est locale, et les fournisseurs l’utilisent en interne afin d’afficher la progression pour les sous-objets de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="36459-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="36459-118">Les objets de progression enregistrent la valeur minimale locale uniquement pour la renvoyer à un fournisseur par le biais d’un appel **GetMin**.</span><span class="sxs-lookup"><span data-stu-id="36459-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="36459-119">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="36459-119">Notes to implementers</span></span>

<span data-ttu-id="36459-120">Initialisez la valeur minimale sur 1.</span><span class="sxs-lookup"><span data-stu-id="36459-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="36459-121">Les fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="36459-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="36459-122">Pour plus d’informations sur la méthode d’implémentation de la méthode **GetMin** et des autres méthodes [IMAPIProgress](imapiprogressiunknown.md), reportez-vous à la rubrique [Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="36459-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="36459-123">Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="36459-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36459-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36459-124">MFCMAPI reference</span></span>

<span data-ttu-id="36459-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="36459-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36459-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="36459-126">**File**</span></span>|<span data-ttu-id="36459-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="36459-127">**Function**</span></span>|<span data-ttu-id="36459-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="36459-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36459-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="36459-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="36459-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="36459-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="36459-131">MFCMAPI utilise la méthode **IMAPIProgress::GetMin** afin d’obtenir la valeur minimale pour l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="36459-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="36459-132">Renvoie la valeur 1 sauf si des limites ont précédemment été définies au moyen de l’appel de la méthode **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="36459-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36459-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36459-133">See also</span></span>



[<span data-ttu-id="36459-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="36459-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="36459-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="36459-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="36459-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="36459-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="36459-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36459-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="36459-138">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="36459-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="36459-139">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="36459-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="36459-140">Implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="36459-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

