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
ms.openlocfilehash: 8964ba8c4341bec431bdbc1690d639b345df8b1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783880"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="54ad5-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="54ad5-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="54ad5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54ad5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54ad5-105">L’indicateur renvoie les paramètres de l’objet de l’avancement du niveau de l’opération sur lequel les informations d’avancement sont calculées.</span><span class="sxs-lookup"><span data-stu-id="54ad5-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="54ad5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54ad5-106">Parameters</span></span>

 <span data-ttu-id="54ad5-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="54ad5-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="54ad5-108">[out] Masque de bits d’indicateurs qui contrôle le niveau de l’opération sur l’avancement des informations sont calculées.</span><span class="sxs-lookup"><span data-stu-id="54ad5-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="54ad5-109">L’indicateur suivantes peut être renvoyées :</span><span class="sxs-lookup"><span data-stu-id="54ad5-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="54ad5-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="54ad5-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="54ad5-111">Progression est calculée pour l’objet de niveau supérieur, l’objet qui est appelée par le client doit commencer l’opération.</span><span class="sxs-lookup"><span data-stu-id="54ad5-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="54ad5-112">Par exemple, l’objet de niveau supérieur dans une opération de copie du dossier est le dossier en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="54ad5-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="54ad5-113">Lorsque MAPI_TOP_LEVEL n’est pas défini, l’avancement est calculé pour un objet de niveau inférieur ou sous-objet.</span><span class="sxs-lookup"><span data-stu-id="54ad5-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="54ad5-114">Dans l’opération de copie de dossier, un objet de niveau inférieur est un des sous-dossiers dans le dossier en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="54ad5-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54ad5-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="54ad5-115">Return value</span></span>

<span data-ttu-id="54ad5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="54ad5-116">S_OK</span></span> 
  
> <span data-ttu-id="54ad5-117">La valeur flags a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="54ad5-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54ad5-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="54ad5-118">Remarks</span></span>

<span data-ttu-id="54ad5-119">MAPI permet aux prestataires de faire la distinction entre les objets de niveau supérieur et sous-objets avec l’indicateur MAPI_TOP_LEVEL afin que tous les objets impliquant dans une opération peuvent utiliser la même implémentation [IMAPIProgress](imapiprogressiunknown.md) pour afficher la progression.</span><span class="sxs-lookup"><span data-stu-id="54ad5-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="54ad5-120">Cela entraîne l’affichage de l’indicateur en douceur dans un seul sens positif.</span><span class="sxs-lookup"><span data-stu-id="54ad5-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="54ad5-121">Si l’indicateur MAPI_TOP_LEVEL est défini détermine comment les fournisseurs de services de définissent les autres paramètres dans les appels suivants à l’objet de l’avancement.</span><span class="sxs-lookup"><span data-stu-id="54ad5-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="54ad5-122">La valeur renvoyée par **GetFlags** est initialement définie par l’implémentation et par la suite par le fournisseur de services via un appel à la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="54ad5-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="54ad5-123">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="54ad5-123">Notes to implementers</span></span>

<span data-ttu-id="54ad5-124">Toujours initialiser l’indicateur MAPI_TOP_LEVEL, puis ils s’appuient sur les fournisseurs de services pour la désactiver le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="54ad5-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="54ad5-125">Fournisseurs de services peuvent supprimer et réinitialiser l’indicateur en appelant la méthode **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="54ad5-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="54ad5-126">Pour plus d’informations sur la façon d’implémenter **GetFlags** et les autres méthodes **IMAPIProgress** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="54ad5-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="54ad5-127">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="54ad5-127">Notes to callers</span></span>

<span data-ttu-id="54ad5-128">Lorsque vous affichez un indicateur de progression, appelez votre premier appel un **IMAPIProgress::GetFlags**.</span><span class="sxs-lookup"><span data-stu-id="54ad5-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="54ad5-129">La valeur renvoyée doit être MAPI_TOP_LEVEL, car toutes les implémentations initialiser le contenu du paramètre _lpulFlags_ à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="54ad5-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="54ad5-130">Pour plus d’informations sur la séquence d’appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="54ad5-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="54ad5-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="54ad5-131">MFCMAPI reference</span></span>

<span data-ttu-id="54ad5-132">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="54ad5-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="54ad5-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="54ad5-133">**File**</span></span>|<span data-ttu-id="54ad5-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="54ad5-134">**Function**</span></span>|<span data-ttu-id="54ad5-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="54ad5-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54ad5-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="54ad5-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="54ad5-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="54ad5-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="54ad5-138">MFCMAPI utilise la méthode **IMAPIProgress::GetFlags** pour déterminer les indicateurs sont définis.</span><span class="sxs-lookup"><span data-stu-id="54ad5-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="54ad5-139">Renvoie MAPI_TOP_LEVEL, sauf si indicateurs ont été définis à l’aide de la méthode **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="54ad5-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54ad5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54ad5-140">See also</span></span>



[<span data-ttu-id="54ad5-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="54ad5-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="54ad5-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54ad5-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="54ad5-143">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="54ad5-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="54ad5-144">Afficher un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="54ad5-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="54ad5-145">L’implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="54ad5-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

