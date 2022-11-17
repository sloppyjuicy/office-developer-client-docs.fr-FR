---
title: Affichage d’un indicateur de progression
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 03bb17b6f547057cc51582c726a2048499eaada6
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465646"
---
# <a name="display-a-progress-indicator"></a>Affichage d’un indicateur de progression
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour afficher un indicateur de progression, appelez [IMAPIProgress::GetFlags](imapiprogress-getflags.md) pour récupérer le paramètre d’indicateurs actuel. 
  
Si l’MAPI_TOP_LEVEL est définie, complétez les étapes suivantes :
  
1. Définir une variable égale au nombre total d’éléments à traiter dans l’opération. Par exemple, si vous copiez le contenu d’un dossier, cette valeur est égale au nombre de sous-dossiers du dossier plus le nombre de messages. 
    
2. Définissez une variable sur 1 000 divisé par le nombre d’éléments. 
    
3. Si vous indiquez la progression des sous-objets, appelez la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) de l’objet de progression et passez les valeurs suivantes pour les trois paramètres : 
    
   - Définissez  _le paramètre lpulMin_ sur 0. 
    
   - Définissez  _le paramètre lpulMax_ sur 1000. 
    
   - Définissez  _le paramètre lpulFlags_ sur MAPI_TOP_LEVEL. 
    
4. Pour chaque objet à traiter, effectuer les étapes suivantes :
    
   1. **Appelez IMAPIProgress::SetLimits** et passez les valeurs suivantes pour les trois paramètres : 
      
     - Définissez  _le paramètre lpulMin_ sur la variable définie à l’étape 2 multipliée par l’élément actuel moins 1. 
      
     - Définissez  _le paramètre lpulMax_ sur la variable définie à l’étape 2 multipliée par l’objet actuel. 
      
     - Définissez  _le paramètre lpulFlags_ sur 0. 
      
   2. Effectuez tout traitement à effectuer sur cet objet. S’il s’agit d’un sous-objet et que vous souhaitez afficher la progression sur les sous-objets, passez un pointeur vers l’objet de progression dans le paramètre _lpProgress_ à la méthode. 
      
   3. [Appelez IMAPIProgress::P rogress](imapiprogress-progress.md) et passez les valeurs suivantes pour les trois paramètres : 
      
     - Définissez  _le paramètre ulValue_ sur la variable définie à l’étape 2 multipliée par l’objet actuel. 
      
     - Définissez  _le paramètre ulCount_ sur l’objet actuel. 
      
     - Définissez  _le paramètre ulTotal_ sur la variable définie à l’étape 1, le nombre total d’objets. 
    
Si l’MAPI_TOP_LEVEL n’est pas définie, complétez les étapes suivantes :
  
1. Appelez la méthode [IMAPIProgress::GetMin](imapiprogress-getmin.md) de l’objet de progression pour récupérer la valeur minimale de l’affichage. 
    
2. [Appelez IMAPIProgress::GetMax](imapiprogress-getmax.md) pour récupérer la valeur maximale de l’affichage. 
    
3. Définissez une variable sur le nombre total d’objets à traiter. 
    
4. Définissez une variable sur le résultat de la soustraction de la valeur minimale de la valeur maximale, puis de la division par le nombre total d’objets.
    
5. Pour chaque objet à traiter, effectuer les étapes suivantes :
    
   1. Si votre fournisseur affiche la progression des sous-objets, appelez **IMAPIProgress::SetLimits** et passez les valeurs suivantes pour les trois paramètres : 
      
     - Définissez  _le paramètre lpulMin_ sur la valeur minimale plus l’élément actuel moins 1 multiplié par la variable définie à l’étape 4. 
      
     - Définissez  _le paramètre lpulMax_ sur la valeur minimale plus l’unité actuelle multipliée par la variable définie à l’étape 4. 
      
     - Définissez  _le paramètre lpulFlags_ sur 0. 
      
   2. Effectuez tout traitement à effectuer sur cet objet. Si l’objet est un sous-objet et que votre fournisseur affiche la progression des sous-objets, passez un pointeur vers l’objet de progression dans le paramètre _lpProgress_ à la méthode. 
      
   3. [Appelez IMAPIProgress::P rogress](imapiprogress-progress.md) et passez les valeurs suivantes pour les trois paramètres : 
      
     - Définissez  _le paramètre ulValue_ sur un jeu de variables à l’étape 2 multiplié par l’objet actuel. 
      
     - Définissez  _le paramètre ulCount_ sur 0. 
      
     - Définissez  _le paramètre ulTotal_ sur 0. 
    
L’exemple de code suivant illustre la logique requise pour afficher la progression à tous les niveaux d’une opération qui copie le contenu d’un dossier qui contient cinq sous-dossiers. 
  
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

