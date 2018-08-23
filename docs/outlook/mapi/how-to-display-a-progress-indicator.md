---
title: Afficher un indicateur de progression
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 62549cbeea0044ceee8aa2e704b8a9bc271b7e8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564492"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="0fb04-103">Afficher un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="0fb04-103">Display a progress indicator</span></span>
 
<span data-ttu-id="0fb04-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fb04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fb04-105">Pour afficher un indicateur de progression, appelez [IMAPIProgress::GetFlags](imapiprogress-getflags.md) pour récupérer les indicateurs en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="0fb04-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="0fb04-106">Si l’indicateur MAPI_TOP_LEVEL est défini, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0fb04-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="0fb04-107">Définir une variable comme étant égale au nombre total d’éléments à traiter de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0fb04-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="0fb04-108">Par exemple, si vous copiez le contenu d’un dossier, cette valeur sera égale au nombre de sous-dossiers dans le dossier ainsi que le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="0fb04-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="0fb04-109">Définir une variable comme étant égale à 1000 divisée par le nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="0fb04-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="0fb04-110">Si l’affichage des cours pour les sous-objets, appelez la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) de l’objet de la progression et passez les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0fb04-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="0fb04-111">Définissez le paramètre _lpulMin_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0fb04-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="0fb04-112">Définissez le paramètre _lpulMax_ et 1000.</span><span class="sxs-lookup"><span data-stu-id="0fb04-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="0fb04-113">La valeur du paramètre _lpulFlags_ MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="0fb04-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="0fb04-114">Pour chaque objet de traitement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0fb04-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="0fb04-115">Appelez **IMAPIProgress::SetLimits** et transmettre les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0fb04-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0fb04-116">Définissez le paramètre _lpulMin_ à la variable définie à l’étape 2 multiplié par l’élément actuel moins 1.</span><span class="sxs-lookup"><span data-stu-id="0fb04-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="0fb04-117">Définissez le paramètre _lpulMax_ à la variable définie à l’étape 2 multiplié par l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0fb04-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0fb04-118">Définissez le paramètre _lpulFlags_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0fb04-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="0fb04-119">Effectuer le traitement doit être effectué sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="0fb04-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="0fb04-120">Si c’est un sous-objet et que vous souhaitez afficher la progression sur sous-objets, passez un pointeur vers l’objet de l’avancement dans le paramètre _lpProgress_ à la méthode.</span><span class="sxs-lookup"><span data-stu-id="0fb04-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="0fb04-121">Appelez [IMAPIProgress::Progress](imapiprogress-progress.md) et transmettre les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0fb04-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0fb04-122">Définissez le paramètre _ulValue_ à la variable définie à l’étape 2 multiplié par l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0fb04-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0fb04-123">Définissez le paramètre _ulCount_ pour l’objet actif.</span><span class="sxs-lookup"><span data-stu-id="0fb04-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="0fb04-124">Définissez le paramètre _ulTotal_ à la variable définie à l’étape 1, le nombre total d’objets.</span><span class="sxs-lookup"><span data-stu-id="0fb04-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="0fb04-125">Si l’indicateur MAPI_TOP_LEVEL n’est pas défini, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0fb04-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="0fb04-126">Appelez la méthode de [IMAPIProgress::GetMin](imapiprogress-getmin.md) de l’objet l’avancement pour récupérer la valeur minimale pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="0fb04-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="0fb04-127">Appelez [IMAPIProgress::GetMax](imapiprogress-getmax.md) pour récupérer la valeur maximale de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="0fb04-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="0fb04-128">Définir une variable comme étant égale au nombre total d’objets à traiter.</span><span class="sxs-lookup"><span data-stu-id="0fb04-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="0fb04-129">Définir une variable est égale au résultat de la soustraction de la valeur minimale de la valeur maximale et en divisant par le nombre total d’objets.</span><span class="sxs-lookup"><span data-stu-id="0fb04-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="0fb04-130">Pour chaque objet de traitement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0fb04-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="0fb04-131">Si votre fournisseur est affichée de progression de sous-objets, appelez **IMAPIProgress::SetLimits** et transmettre les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0fb04-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0fb04-132">Définissez le paramètre _lpulMin_ à la valeur minimale ainsi que l’élément actuel moins 1 multiplié par la variable définie à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="0fb04-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="0fb04-133">Définissez le paramètre _lpulMax_ à la valeur minimale ainsi que l’unité actuelle multiplié par la variable définie à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="0fb04-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="0fb04-134">Définissez le paramètre _lpulFlags_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0fb04-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="0fb04-135">Effectuer le traitement doit être effectué sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="0fb04-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="0fb04-136">Si l’objet est un sous-objet et votre fournisseur affiche la progression de sous-objets, passez un pointeur vers l’objet de l’avancement dans le paramètre _lpProgress_ à la méthode.</span><span class="sxs-lookup"><span data-stu-id="0fb04-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="0fb04-137">Appelez [IMAPIProgress::Progress](imapiprogress-progress.md) et transmettre les valeurs suivantes pour les trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="0fb04-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0fb04-138">Définir le paramètre _ulValue_ variable définie à l’étape 2 multiplié par l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0fb04-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0fb04-139">Définissez le paramètre _ulCount_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0fb04-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="0fb04-140">Définissez le paramètre _ulTotal_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="0fb04-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="0fb04-141">L’exemple de code suivant illustre la logique requise pour afficher la progression à tous les niveaux d’une opération de copie le contenu d’un dossier qui contient les sous-dossiers de cinq.</span><span class="sxs-lookup"><span data-stu-id="0fb04-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="0fb04-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fb04-142">See also</span></span>

- [<span data-ttu-id="0fb04-143">Indicateurs de progression MAPI</span><span class="sxs-lookup"><span data-stu-id="0fb04-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

