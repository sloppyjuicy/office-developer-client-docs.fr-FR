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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2dadad410b9aaf1401d792de373e561c29183a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567236"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="e3f5f-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="e3f5f-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="e3f5f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3f5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3f5f-105">Renvoie le nombre maximal d’éléments dans l’opération de l’avancement des informations s’affichent.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="e3f5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3f5f-106">Parameters</span></span>

 <span data-ttu-id="e3f5f-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="e3f5f-107">_lpulMax_</span></span>
  
> <span data-ttu-id="e3f5f-108">[out] Pointeur vers le nombre maximal d’éléments dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3f5f-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e3f5f-109">Return value</span></span>

<span data-ttu-id="e3f5f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3f5f-110">S_OK</span></span> 
  
> <span data-ttu-id="e3f5f-111">Le nombre maximal d’éléments dans l’opération a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3f5f-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3f5f-112">Remarks</span></span>

<span data-ttu-id="e3f5f-113">La valeur maximale représente la fin de l’opération sous forme numérique.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="e3f5f-114">La valeur peut être une valeur maximale globale, utilisé pour représenter l’étendue de l’affichage de la progression de l’intégralité ou une valeur locale, utilisé pour ne représenter qu’une partie de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="e3f5f-115">La valeur du paramètre indicateur affecte si l’objet de l’avancement comprend la valeur maximale à être local ou global.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="e3f5f-116">Lorsque l’indicateur MAPI_TOP_LEVEL est défini, la valeur maximale est considéré comme étant global et est utilisée pour calculer l’avancement pour toute l’opération.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="e3f5f-117">Lorsque MAPI_TOP_LEVEL n’est pas définie, la valeur maximale est considéré comme étant local, et fournisseurs de l’utiliser en interne pour afficher la progression de sous-objets de niveau inférieurs.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="e3f5f-118">Objets de progression enregistrement la valeur maximale locale uniquement pour renvoyer à un fournisseur via un appel **GetMax** .</span><span class="sxs-lookup"><span data-stu-id="e3f5f-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="e3f5f-119">Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="e3f5f-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e3f5f-120">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e3f5f-120">Notes to implementers</span></span>

<span data-ttu-id="e3f5f-121">Initialiser la valeur maximale et 1000.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="e3f5f-122">Fournisseurs de services peuvent réinitialiser cette valeur en appelant la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="e3f5f-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="e3f5f-123">Pour plus d’informations sur l’implémentation des autres méthodes [IMAPIProgress](imapiprogressiunknown.md) et **GetMax** , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="e3f5f-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e3f5f-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e3f5f-124">MFCMAPI reference</span></span>

<span data-ttu-id="e3f5f-125">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e3f5f-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e3f5f-126">**File**</span></span>|<span data-ttu-id="e3f5f-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e3f5f-127">**Function**</span></span>|<span data-ttu-id="e3f5f-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e3f5f-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3f5f-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="e3f5f-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="e3f5f-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="e3f5f-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="e3f5f-131">MFCMAPI utilise la méthode **IMAPIProgress::GetMax** pour obtenir la valeur maximale pour l’objet de progression.</span><span class="sxs-lookup"><span data-stu-id="e3f5f-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="e3f5f-132">Renvoie 1000, sauf si les limites précédemment ont été définies avec la méthode **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="e3f5f-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3f5f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3f5f-133">See also</span></span>



[<span data-ttu-id="e3f5f-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="e3f5f-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="e3f5f-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="e3f5f-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="e3f5f-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="e3f5f-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="e3f5f-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3f5f-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="e3f5f-138">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e3f5f-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e3f5f-139">Afficher un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="e3f5f-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="e3f5f-140">Implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="e3f5f-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

