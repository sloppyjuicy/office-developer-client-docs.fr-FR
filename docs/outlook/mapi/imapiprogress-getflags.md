---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270266"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="1b7be-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="1b7be-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="1b7be-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b7be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b7be-105">Renvoie les paramètres d'indicateur à partir de l'objet de progression pour le niveau d'opération sur lequel les informations de progression sont calculées.</span><span class="sxs-lookup"><span data-stu-id="1b7be-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1b7be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b7be-106">Parameters</span></span>

 <span data-ttu-id="1b7be-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b7be-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1b7be-108">remarquer Masque de des indicateurs qui contrôle le niveau d'opération sur lequel les informations de progression sont calculées.</span><span class="sxs-lookup"><span data-stu-id="1b7be-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="1b7be-109">L'indicateur suivant peut être renvoyé:</span><span class="sxs-lookup"><span data-stu-id="1b7be-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="1b7be-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="1b7be-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="1b7be-111">La progression est calculée pour l'objet de niveau supérieur, l'objet qui est appelé par le client pour commencer l'opération.</span><span class="sxs-lookup"><span data-stu-id="1b7be-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="1b7be-112">Par exemple, l'objet de niveau supérieur dans une opération de copie de dossier est le dossier en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="1b7be-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="1b7be-113">Lorsque MAPI_TOP_LEVEL n'est pas défini, Progress est calculé pour un objet de niveau inférieur ou un sous-objet.</span><span class="sxs-lookup"><span data-stu-id="1b7be-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="1b7be-114">Dans l'opération de copie de dossier, un objet de niveau inférieur est l'un des sous-dossiers dans le dossier en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="1b7be-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b7be-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b7be-115">Return value</span></span>

<span data-ttu-id="1b7be-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b7be-116">S_OK</span></span> 
  
> <span data-ttu-id="1b7be-117">La valeur flags a été renvoyée.</span><span class="sxs-lookup"><span data-stu-id="1b7be-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b7be-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b7be-118">Remarks</span></span>

<span data-ttu-id="1b7be-119">MAPI permet aux fournisseurs de services de différencier les objets de niveau supérieur et les sous-objets à l'aide de l'indicateur MAPI_TOP_LEVEL afin que tous les objets impliqués dans une opération puissent utiliser la même implémentation [méthode imapiprogress](imapiprogressiunknown.md) pour afficher la progression.</span><span class="sxs-lookup"><span data-stu-id="1b7be-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="1b7be-120">Ainsi, l'indicateur s'affiche en douceur dans une seule direction positive.</span><span class="sxs-lookup"><span data-stu-id="1b7be-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="1b7be-121">La définition de l'indicateur MAPI_TOP_LEVEL détermine la façon dont les fournisseurs de services définissent les autres paramètres dans les appels ultérieurs à l'objet Progress.</span><span class="sxs-lookup"><span data-stu-id="1b7be-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="1b7be-122">La valeur renvoyée par **GetFlags** est initialement définie par l'implémenteur et par la suite par le fournisseur de services par le biais d'un appel à la méthode [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="1b7be-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1b7be-123">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="1b7be-123">Notes to implementers</span></span>

<span data-ttu-id="1b7be-124">Initialisez toujours l'indicateur sur MAPI_TOP_LEVEL, puis faites en sorte que les fournisseurs de services l'efface lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1b7be-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="1b7be-125">Les fournisseurs de services peuvent effacer et réinitialiser l'indicateur en appelant la méthode **méthode imapiprogress:: SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="1b7be-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="1b7be-126">Pour plus d'informations sur la façon d'implémenter **GetFlags** et les autres méthodes **méthode imapiprogress** , consultez la rubrique [implémentation d'un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1b7be-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b7be-127">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="1b7be-127">Notes to callers</span></span>

<span data-ttu-id="1b7be-128">Lorsque vous affichez un indicateur de progression, appelez d'abord un appel à **méthode imapiprogress:: GetFlags**.</span><span class="sxs-lookup"><span data-stu-id="1b7be-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="1b7be-129">La valeur renvoyée doit être MAPI_TOP_LEVEL, car toutes les implémentations initialisent le contenu du paramètre _lpulFlags_ à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="1b7be-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="1b7be-130">Pour plus d'informations sur la séquence d'appels à un objet Progress, voir [afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1b7be-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1b7be-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1b7be-131">MFCMAPI reference</span></span>

<span data-ttu-id="1b7be-132">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b7be-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1b7be-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1b7be-133">**File**</span></span>|<span data-ttu-id="1b7be-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1b7be-134">**Function**</span></span>|<span data-ttu-id="1b7be-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1b7be-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b7be-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="1b7be-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="1b7be-137">CMAPIProgress:: GetFlags</span><span class="sxs-lookup"><span data-stu-id="1b7be-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="1b7be-138">MFCMAPI utilise la méthode **méthode imapiprogress:: GetFlags** pour déterminer les indicateurs définis.</span><span class="sxs-lookup"><span data-stu-id="1b7be-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="1b7be-139">Renvoie MAPI_TOP_LEVEL sauf si les indicateurs ont été définis à l'aide de la méthode **méthode imapiprogress:: SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="1b7be-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b7be-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b7be-140">See also</span></span>



[<span data-ttu-id="1b7be-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="1b7be-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="1b7be-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b7be-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="1b7be-143">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="1b7be-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1b7be-144">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="1b7be-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="1b7be-145">Implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="1b7be-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

