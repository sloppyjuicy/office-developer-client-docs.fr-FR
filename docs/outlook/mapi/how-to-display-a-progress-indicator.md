---
title: Affichage d’un indicateur de progression
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408025"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="0155c-103">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="0155c-103">Display a progress indicator</span></span>
 
<span data-ttu-id="0155c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0155c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0155c-105">Pour afficher un indicateur de progression, appelez [IMAPIProgress::GetFlags](imapiprogress-getflags.md) pour récupérer le paramètre d’indicateurs actuel.</span><span class="sxs-lookup"><span data-stu-id="0155c-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="0155c-106">Si l’MAPI_TOP_LEVEL est définie, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0155c-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="0155c-107">Définissez une variable sur le nombre total d’éléments à traiter dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="0155c-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="0155c-108">Par exemple, si vous copiez le contenu d’un dossier, cette valeur est égale au nombre de sous-dossiers du dossier plus le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="0155c-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="0155c-109">Définissez une variable sur 1 000 divisé par le nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="0155c-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="0155c-110">Si vous indiquez la progression des sous-objets, appelez la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) de l’objet de progression et passez les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0155c-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="0155c-111">Définissez  _le paramètre lpulMin_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0155c-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="0155c-112">Définissez  _le paramètre lpulMax_ sur 1000.</span><span class="sxs-lookup"><span data-stu-id="0155c-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="0155c-113">Définissez  _le paramètre lpulFlags_ sur MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="0155c-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="0155c-114">Pour chaque objet à traiter, effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0155c-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="0155c-115">Appelez **IMAPIProgress::SetLimits** et passez les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0155c-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0155c-116">Définissez  _le paramètre lpulMin_ sur la variable définie à l’étape 2 multipliée par l’élément actuel moins 1.</span><span class="sxs-lookup"><span data-stu-id="0155c-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="0155c-117">Définissez  _le paramètre lpulMax_ sur la variable définie à l’étape 2 multipliée par l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0155c-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0155c-118">Définissez  _le paramètre lpulFlags_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0155c-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="0155c-119">Effectuez tout traitement à effectuer sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="0155c-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="0155c-120">S’il s’agit d’un sous-objet et que vous souhaitez afficher la progression sur les sous-objets, passez un pointeur vers l’objet de progression dans le paramètre  _lpProgress_ à la méthode.</span><span class="sxs-lookup"><span data-stu-id="0155c-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="0155c-121">Appelez [IMAPIProgress::P rogress](imapiprogress-progress.md) et passez les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0155c-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0155c-122">Définissez  _le paramètre ulValue_ sur la variable définie à l’étape 2 multipliée par l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0155c-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0155c-123">Définissez  _le paramètre ulCount_ sur l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0155c-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="0155c-124">Définissez  _le paramètre ulTotal_ sur la variable définie à l’étape 1, le nombre total d’objets.</span><span class="sxs-lookup"><span data-stu-id="0155c-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="0155c-125">Si l’MAPI_TOP_LEVEL n’est pas définie, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0155c-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="0155c-126">Appelez la méthode [IMAPIProgress::GetMin](imapiprogress-getmin.md) de l’objet de progression pour récupérer la valeur minimale de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="0155c-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="0155c-127">Appelez [IMAPIProgress::GetMax](imapiprogress-getmax.md) pour récupérer la valeur maximale de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="0155c-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="0155c-128">Définissez une variable sur le nombre total d’objets à traiter.</span><span class="sxs-lookup"><span data-stu-id="0155c-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="0155c-129">Définissez une variable sur le résultat de la soustraction de la valeur minimale de la valeur maximale, puis de la division par le nombre total d’objets.</span><span class="sxs-lookup"><span data-stu-id="0155c-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="0155c-130">Pour chaque objet à traiter, effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0155c-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="0155c-131">Si votre fournisseur affiche la progression des sous-objets, appelez **IMAPIProgress::SetLimits** et passez les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0155c-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0155c-132">Définissez  _le paramètre lpulMin_ sur la valeur minimale plus l’élément actuel moins 1 multiplié par la variable définie à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="0155c-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="0155c-133">Définissez  _le paramètre lpulMax_ sur la valeur minimale plus l’unité actuelle multipliée par la variable définie à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="0155c-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="0155c-134">Définissez  _le paramètre lpulFlags_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0155c-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="0155c-135">Effectuez tout traitement à effectuer sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="0155c-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="0155c-136">Si l’objet est un sous-objet et que votre fournisseur affiche la progression des sous-objets, passez un pointeur vers l’objet de progression dans le paramètre  _lpProgress_ à la méthode.</span><span class="sxs-lookup"><span data-stu-id="0155c-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="0155c-137">Appelez [IMAPIProgress::P rogress](imapiprogress-progress.md) et passez les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0155c-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0155c-138">Définissez  _le paramètre ulValue_ sur variable définie à l’étape 2 multipliée par l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0155c-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0155c-139">Définissez  _le paramètre ulCount_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0155c-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="0155c-140">Définissez  _le paramètre ulTotal_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0155c-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="0155c-141">L’exemple de code suivant illustre la logique requise pour afficher la progression à tous les niveaux d’une opération qui copie le contenu d’un dossier qui contient cinq sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="0155c-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a><span data-ttu-id="0155c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0155c-142">See also</span></span>

- [<span data-ttu-id="0155c-143">Indicateurs de progression MAPI</span><span class="sxs-lookup"><span data-stu-id="0155c-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

