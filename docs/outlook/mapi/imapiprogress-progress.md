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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435494"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="e0cd2-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="e0cd2-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="e0cd2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0cd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0cd2-105">Met à jour l'indicateur de progression avec un affichage de la progression au fur et à mesure de l'exécution de l'opération.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="e0cd2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0cd2-106">Parameters</span></span>

 <span data-ttu-id="e0cd2-107">_Objet_</span><span class="sxs-lookup"><span data-stu-id="e0cd2-107">_ulValue_</span></span>
  
> <span data-ttu-id="e0cd2-108">dans Nombre qui indique le niveau actuel de progression (calculé à partir des paramètres _ulCount_ et _ulTotal_ ou à partir des paramètres _lpulMin_ et _LpulMax_ de la méthode [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md) ) entre le Global limite inférieure et limite supérieure globale.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="e0cd2-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="e0cd2-109">_ulCount_</span></span>
  
> <span data-ttu-id="e0cd2-110">dans Nombre indiquant l'élément actuellement traité par rapport au total.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="e0cd2-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="e0cd2-111">_ulTotal_</span></span>
  
> <span data-ttu-id="e0cd2-112">dans Nombre total d'éléments à traiter au cours de l'opération.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0cd2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e0cd2-113">Return value</span></span>

<span data-ttu-id="e0cd2-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0cd2-114">S_OK</span></span> 
  
> <span data-ttu-id="e0cd2-115">L'indicateur de progression a été mis à jour avec succès.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e0cd2-116">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e0cd2-116">Notes to implementers</span></span>

<span data-ttu-id="e0cd2-117">Le paramètre _ulValue_ est égal à la valeur minimale globale uniquement au début de l'opération et à la valeur maximale globale uniquement à la fin de l'opération.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="e0cd2-118">Utilisez les paramètres _ulCount_ et _ulTotal_ , s'ils sont disponibles, pour afficher un message facultatif, par exemple, «5 éléments terminés sur 10».</span><span class="sxs-lookup"><span data-stu-id="e0cd2-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="e0cd2-119">Si _ulCount_ et _ulTotal_ sont définis sur 0, déterminez si l'indicateur de progression doit être modifié visuellement.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="e0cd2-120">Certains fournisseurs de services définissent ces paramètres sur 0 pour indiquer qu'ils traitent un sous-objet dont la progression est contrôlée par rapport à un objet parent.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="e0cd2-121">Dans ce cas, il est logique de modifier l'affichage uniquement lorsque l'objet parent indique la progression.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="e0cd2-122">Certains fournisseurs de services transfèrent 0 pour ces paramètres à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="e0cd2-123">Pour plus d'informations sur la façon d'implémenter la **progression** et les autres méthodes [méthode imapiprogress](imapiprogressiunknown.md) , consultez la rubrique [implémentation d'un indicateur de progression](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="e0cd2-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e0cd2-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e0cd2-124">Notes to callers</span></span>

<span data-ttu-id="e0cd2-125">Les trois paramètres de **méthode imapiprogress::P rogress** sont tous obligatoires.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="e0cd2-126">Le seul paramètre obligatoire est _ulValue_, un nombre qui indique le pourcentage d'avancement.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="e0cd2-127">Si l'indicateur MAPI_TOP_LEVEL est défini, vous pouvez également transmettre un nombre d'objets et un total d'objets.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="e0cd2-128">Certaines implémentations utilisent ces valeurs pour afficher une phrase telle que «5 éléments terminés sur 10» avec l'indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="e0cd2-129">Si vous copiez tous les messages dans un seul dossier, définissez _ulTotal_ sur le nombre total de messages en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="e0cd2-130">Si vous copiez un dossier, définissez _ulTotal_ sur le nombre de sous-dossiers dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="e0cd2-131">Si le dossier à copier ne contient pas de sous-dossiers ni de messages, affectez la valeur 1 à _ulTotal_ .</span><span class="sxs-lookup"><span data-stu-id="e0cd2-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="e0cd2-132">Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="e0cd2-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0cd2-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e0cd2-133">MFCMAPI reference</span></span>

<span data-ttu-id="e0cd2-134">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0cd2-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e0cd2-135">**File**</span></span>|<span data-ttu-id="e0cd2-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e0cd2-136">**Function**</span></span>|<span data-ttu-id="e0cd2-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e0cd2-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0cd2-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="e0cd2-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="e0cd2-139">CMAPIProgress::P rogress</span><span class="sxs-lookup"><span data-stu-id="e0cd2-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="e0cd2-140">MFCMAPI utilise la méthode **méthode imapiprogress::P rogress** pour mettre à jour la barre d'état de MFCMAPI avec le pourcentage d'avancement actuel, calculé à partir de _uValue_ et les valeurs maximale et minimale actuelles.</span><span class="sxs-lookup"><span data-stu-id="e0cd2-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0cd2-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0cd2-141">See also</span></span>



[<span data-ttu-id="e0cd2-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="e0cd2-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="e0cd2-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0cd2-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="e0cd2-144">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="e0cd2-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e0cd2-145">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="e0cd2-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="e0cd2-146">Implémentation d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="e0cd2-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

