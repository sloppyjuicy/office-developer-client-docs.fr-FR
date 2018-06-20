---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2a003be35fc9c3ef8efc7c66997ee99f6e578f09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783886"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="059e9-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="059e9-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="059e9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="059e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="059e9-105">Met à jour l’indicateur de progression avec un affichage de la progression qu’elle est réalisée vers la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="059e9-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="059e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="059e9-106">Parameters</span></span>

 <span data-ttu-id="059e9-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="059e9-107">_ulValue_</span></span>
  
> <span data-ttu-id="059e9-108">[in] Un nombre qui indique le niveau actuel de l’avancement (calculée à partir des paramètres _ulCount_ et _ulTotal_ ou à partir des paramètres de la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) _lpulMin_ et _lpulMax_ ) entre le modèle global limite inférieure et la limite supérieure globale.</span><span class="sxs-lookup"><span data-stu-id="059e9-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="059e9-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="059e9-109">_ulCount_</span></span>
  
> <span data-ttu-id="059e9-110">[in] Nombre qui indique l’élément actuellement traitée par rapport au total.</span><span class="sxs-lookup"><span data-stu-id="059e9-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="059e9-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="059e9-111">_ulTotal_</span></span>
  
> <span data-ttu-id="059e9-112">[in] Nombre total d’éléments à être traités au cours de l’opération.</span><span class="sxs-lookup"><span data-stu-id="059e9-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="059e9-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="059e9-113">Return value</span></span>

<span data-ttu-id="059e9-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="059e9-114">S_OK</span></span> 
  
> <span data-ttu-id="059e9-115">L’indicateur de progression a été correctement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="059e9-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="059e9-116">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="059e9-116">Notes to implementers</span></span>

<span data-ttu-id="059e9-117">Le paramètre _ulValue_ est égal à la valeur minimale globale uniquement au début de l’opération et à la valeur maximale globale uniquement à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="059e9-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="059e9-118">Utiliser les paramètres _ulCount_ et _ulTotal_ , le cas échéant afficher un message facultatif, tel que « 5 éléments terminé sur 10 ».</span><span class="sxs-lookup"><span data-stu-id="059e9-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="059e9-119">Si _ulCount_ et _ulTotal_ sont définies à 0, décider s’il faut modifier visuellement l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="059e9-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="059e9-120">Certains fournisseurs de services de définissent ces paramètres à 0 pour indiquer qu’ils sont traitement un sous-objet dont la progression est surveillée par rapport à un objet parent.</span><span class="sxs-lookup"><span data-stu-id="059e9-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="059e9-121">Dans ce cas, il est logique de modifier l’affichage uniquement lorsque l’objet parent signale la progression.</span><span class="sxs-lookup"><span data-stu-id="059e9-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="059e9-122">Certains fournisseurs de services passez 0 pour ces paramètres à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="059e9-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="059e9-123">Pour plus d’informations sur l’implémentation de **progression** et les autres méthodes [IMAPIProgress](imapiprogressiunknown.md) , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="059e9-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="059e9-124">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="059e9-124">Notes to callers</span></span>

<span data-ttu-id="059e9-125">Trois pas tous les paramètres **IMAPIProgress::Progress** sont requis.</span><span class="sxs-lookup"><span data-stu-id="059e9-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="059e9-126">Le seul paramètre requis est un _objet ulValue_, un nombre qui indique le pourcentage d’avancement.</span><span class="sxs-lookup"><span data-stu-id="059e9-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="059e9-127">Si l’indicateur MAPI_TOP_LEVEL est défini, vous pouvez également passer un nombre d’objets et un total de l’objet.</span><span class="sxs-lookup"><span data-stu-id="059e9-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="059e9-128">Certaines implémentations utilisent ces valeurs pour afficher une phrase tel que « 5 éléments terminé sur 10 » avec l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="059e9-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="059e9-129">Si vous copiez tous les messages dans un dossier unique, définissez _ulTotal_ et le nombre total de messages en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="059e9-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="059e9-130">Si vous copiez un dossier, définissez _ulTotal_ au nombre de sous-dossiers dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="059e9-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="059e9-131">Si le dossier à copier ne contient aucun uniquement les messages et les sous-dossiers, _ulTotal_ la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="059e9-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="059e9-132">Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="059e9-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="059e9-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="059e9-133">MFCMAPI reference</span></span>

<span data-ttu-id="059e9-134">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="059e9-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="059e9-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="059e9-135">**File**</span></span>|<span data-ttu-id="059e9-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="059e9-136">**Function**</span></span>|<span data-ttu-id="059e9-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="059e9-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="059e9-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="059e9-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="059e9-139">CMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="059e9-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="059e9-140">MFCMAPI utilise la méthode **IMAPIProgress::Progress** pour mettre à jour de la barre d’état MFCMAPI avec le pourcentage d’avancement, calculée à partir de _uValue_ et les valeurs maximales et minimales en cours.</span><span class="sxs-lookup"><span data-stu-id="059e9-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="059e9-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="059e9-141">See also</span></span>



[<span data-ttu-id="059e9-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="059e9-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="059e9-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="059e9-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="059e9-144">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="059e9-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="059e9-145">Afficher un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="059e9-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="059e9-146">L’implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="059e9-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

