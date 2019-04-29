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
# <a name="display-a-progress-indicator"></a><span data-ttu-id="d0ce5-103">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="d0ce5-103">Display a progress indicator</span></span>
 
<span data-ttu-id="d0ce5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0ce5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0ce5-105">Pour afficher un indicateur de progression, appelez [méthode imapiprogress:: GetFlags](imapiprogress-getflags.md) pour extraire le paramètre Current Flags.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="d0ce5-106">Si l'indicateur MAPI_TOP_LEVEL est défini, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="d0ce5-107">Définissez une variable égale au nombre total d'éléments à traiter dans l'opération.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="d0ce5-108">Par exemple, si vous copiez le contenu d'un dossier, cette valeur est égale au nombre de sous-dossiers dans le dossier, suivi du nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="d0ce5-109">Définissez une variable égale à 1000 divisée par le nombre d'éléments.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="d0ce5-110">Si vous affichez la progression des sous-objets, appelez la méthode [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md) de l'objet Progress et transmettez les valeurs suivantes pour les trois paramètres:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="d0ce5-111">Définissez le paramètre _lpulMin_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="d0ce5-112">Définissez le paramètre _lpulMax_ sur 1000.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="d0ce5-113">Définissez le paramètre _lpulFlags_ sur MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="d0ce5-114">Pour chaque objet à traiter, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="d0ce5-115">Appelez **méthode imapiprogress:: SetLimits** et transmettez les valeurs suivantes pour les trois paramètres:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="d0ce5-116">Définissez le paramètre _lpulMin_ sur la variable définie à l'étape 2 multipliée par l'élément actuel moins 1.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="d0ce5-117">Définissez le paramètre _lpulMax_ sur la variable définie à l'étape 2 multipliée par l'objet actif.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="d0ce5-118">Définissez le paramètre _lpulFlags_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="d0ce5-119">Exécutez le traitement qui doit être effectué sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="d0ce5-120">S'il s'agit d'un sous-objet et que vous souhaitez afficher la progression des sous-objets, transférez un pointeur vers l'objet Progress dans le paramètre _lpProgress_ vers la méthode.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="d0ce5-121">Appelez [méthode imapiprogress::P rogress](imapiprogress-progress.md) et transmettez les valeurs suivantes pour les trois paramètres:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="d0ce5-122">Définissez le paramètre _ulValue_ sur la variable définie à l'étape 2 multipliée par l'objet actif.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="d0ce5-123">Définissez le paramètre _ulCount_ sur l'objet actif.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="d0ce5-124">Définissez le paramètre _ulTotal_ sur la variable définie à l'étape 1, le nombre total d'objets.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="d0ce5-125">Si l'indicateur MAPI_TOP_LEVEL n'est pas défini, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="d0ce5-126">Appelez la méthode [méthode imapiprogress:: GetMin](imapiprogress-getmin.md) de l'objet de progression pour extraire la valeur minimale pour l'affichage.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="d0ce5-127">Appelez [méthode imapiprogress:: GetMax](imapiprogress-getmax.md) pour récupérer la valeur maximale de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="d0ce5-128">Définissez une variable égale au nombre total d'objets à traiter.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="d0ce5-129">Définissez une variable égale au résultat obtenu en soustrayant la valeur minimale de la valeur maximale, puis en divisant le nombre total d'objets.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="d0ce5-130">Pour chaque objet à traiter, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="d0ce5-131">Si votre fournisseur affiche la progression des sous-objets, appelez **méthode imapiprogress:: SetLimits** et transmettez les valeurs suivantes pour les trois paramètres:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="d0ce5-132">Définissez le paramètre _lpulMin_ sur la valeur minimale plus l'élément actif moins 1 multiplié par la variable définie à l'étape 4.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="d0ce5-133">Définissez le paramètre _lpulMax_ sur la valeur minimale plus l'unité actuelle multipliée par la variable définie à l'étape 4.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="d0ce5-134">Définissez le paramètre _lpulFlags_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="d0ce5-135">Exécutez le traitement qui doit être effectué sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="d0ce5-136">Si l'objet est un sous-objet et que votre fournisseur affiche la progression des sous-objets, transmettez un pointeur vers l'objet Progress dans le paramètre _lpProgress_ à la méthode.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="d0ce5-137">Appelez [méthode imapiprogress::P rogress](imapiprogress-progress.md) et transmettez les valeurs suivantes pour les trois paramètres:</span><span class="sxs-lookup"><span data-stu-id="d0ce5-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="d0ce5-138">Définissez le paramètre _ulValue_ sur variable définie à l'étape 2 multipliée par l'objet actif.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="d0ce5-139">Définissez le paramètre _ulCount_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="d0ce5-140">Définissez le paramètre _ulTotal_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="d0ce5-141">L'exemple de code suivant illustre la logique requise pour afficher la progression à tous les niveaux d'une opération qui copie le contenu d'un dossier contenant cinq sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="d0ce5-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="d0ce5-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0ce5-142">See also</span></span>

- [<span data-ttu-id="d0ce5-143">Indicateurs de progression MAPI</span><span class="sxs-lookup"><span data-stu-id="d0ce5-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

