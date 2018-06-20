---
title: Afficher un indicateur de progression
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3c4c553a000dab233eb208c1222cc427c97b1e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783474"
---
# <a name="display-a-progress-indicator"></a>Afficher un indicateur de progression
 
**S’applique à**: Outlook 
  
Pour afficher un indicateur de progression, appelez [IMAPIProgress::GetFlags](imapiprogress-getflags.md) pour récupérer les indicateurs en cours de définition. 
  
Si l’indicateur MAPI_TOP_LEVEL est défini, procédez comme suit :
  
1. Définir une variable comme étant égale au nombre total d’éléments à traiter de l’opération. Par exemple, si vous copiez le contenu d’un dossier, cette valeur sera égale au nombre de sous-dossiers dans le dossier ainsi que le nombre de messages. 
    
2. Définir une variable comme étant égale à 1000 divisée par le nombre d’éléments. 
    
3. Si l’affichage des cours pour les sous-objets, appelez la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) de l’objet de la progression et passez les valeurs suivantes pour les trois paramètres : 
    
   - Définissez le paramètre _lpulMin_ sur 0. 
    
   - Définissez le paramètre _lpulMax_ et 1000. 
    
   - La valeur du paramètre _lpulFlags_ MAPI_TOP_LEVEL. 
    
4. Pour chaque objet de traitement, procédez comme suit :
    
   1. Appelez **IMAPIProgress::SetLimits** et transmettre les valeurs suivantes pour les trois paramètres : 
      
     - Définissez le paramètre _lpulMin_ à la variable définie à l’étape 2 multiplié par l’élément actuel moins 1. 
      
     - Définissez le paramètre _lpulMax_ à la variable définie à l’étape 2 multiplié par l’objet actuel. 
      
     - Définissez le paramètre _lpulFlags_ sur 0. 
      
   2. Effectuer le traitement doit être effectué sur cet objet. Si c’est un sous-objet et que vous souhaitez afficher la progression sur sous-objets, passez un pointeur vers l’objet de l’avancement dans le paramètre _lpProgress_ à la méthode. 
      
   3. Appelez [IMAPIProgress::Progress](imapiprogress-progress.md) et transmettre les valeurs suivantes pour les trois paramètres : 
      
     - Définissez le paramètre _ulValue_ à la variable définie à l’étape 2 multiplié par l’objet actuel. 
      
     - Définissez le paramètre _ulCount_ pour l’objet actif. 
      
     - Définissez le paramètre _ulTotal_ à la variable définie à l’étape 1, le nombre total d’objets. 
    
Si l’indicateur MAPI_TOP_LEVEL n’est pas défini, procédez comme suit :
  
1. Appelez la méthode de [IMAPIProgress::GetMin](imapiprogress-getmin.md) de l’objet l’avancement pour récupérer la valeur minimale pour l’affichage. 
    
2. Appelez [IMAPIProgress::GetMax](imapiprogress-getmax.md) pour récupérer la valeur maximale de l’affichage. 
    
3. Définir une variable comme étant égale au nombre total d’objets à traiter. 
    
4. Définir une variable est égale au résultat de la soustraction de la valeur minimale de la valeur maximale et en divisant par le nombre total d’objets.
    
5. Pour chaque objet de traitement, procédez comme suit :
    
   1. Si votre fournisseur est affichée de progression de sous-objets, appelez **IMAPIProgress::SetLimits** et transmettre les valeurs suivantes pour les trois paramètres : 
      
     - Définissez le paramètre _lpulMin_ à la valeur minimale ainsi que l’élément actuel moins 1 multiplié par la variable définie à l’étape 4. 
      
     - Définissez le paramètre _lpulMax_ à la valeur minimale ainsi que l’unité actuelle multiplié par la variable définie à l’étape 4. 
      
     - Définissez le paramètre _lpulFlags_ sur 0. 
      
   2. Effectuer le traitement doit être effectué sur cet objet. Si l’objet est un sous-objet et votre fournisseur affiche la progression de sous-objets, passez un pointeur vers l’objet de l’avancement dans le paramètre _lpProgress_ à la méthode. 
      
   3. Appelez [IMAPIProgress::Progress](imapiprogress-progress.md) et transmettre les valeurs suivantes pour les trois paramètres : 
      
     - Définir le paramètre _ulValue_ variable définie à l’étape 2 multiplié par l’objet actuel. 
      
     - Définissez le paramètre _ulCount_ sur 0. 
      
     - Définissez le paramètre _ulTotal_ sur 0. 
    
L’exemple de code suivant illustre la logique requise pour afficher la progression à tous les niveaux d’une opération de copie le contenu d’un dossier qui contient les sous-dossiers de cinq. 
  
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

## <a name="see-also"></a>Voir aussi

- [Indicateurs de progression MAPI](mapi-progress-indicators.md)

