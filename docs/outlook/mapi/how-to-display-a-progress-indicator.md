---
title: Affichage d’un indicateur de progression
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345128"
---
# <a name="display-a-progress-indicator"></a>Affichage d’un indicateur de progression
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour afficher un indicateur de progression, appelez [méthode imapiprogress:: GetFlags](imapiprogress-getflags.md) pour extraire le paramètre Current Flags. 
  
Si l'indicateur MAPI_TOP_LEVEL est défini, procédez comme suit:
  
1. Définissez une variable égale au nombre total d'éléments à traiter dans l'opération. Par exemple, si vous copiez le contenu d'un dossier, cette valeur est égale au nombre de sous-dossiers dans le dossier, suivi du nombre de messages. 
    
2. Définissez une variable égale à 1000 divisée par le nombre d'éléments. 
    
3. Si vous affichez la progression des sous-objets, appelez la méthode [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md) de l'objet Progress et transmettez les valeurs suivantes pour les trois paramètres: 
    
   - Définissez le paramètre _lpulMin_ sur 0. 
    
   - Définissez le paramètre _lpulMax_ sur 1000. 
    
   - Définissez le paramètre _lpulFlags_ sur MAPI_TOP_LEVEL. 
    
4. Pour chaque objet à traiter, procédez comme suit:
    
   1. Appelez **méthode imapiprogress:: SetLimits** et transmettez les valeurs suivantes pour les trois paramètres: 
      
     - Définissez le paramètre _lpulMin_ sur la variable définie à l'étape 2 multipliée par l'élément actuel moins 1. 
      
     - Définissez le paramètre _lpulMax_ sur la variable définie à l'étape 2 multipliée par l'objet actif. 
      
     - Définissez le paramètre _lpulFlags_ sur 0. 
      
   2. Exécutez le traitement qui doit être effectué sur cet objet. S'il s'agit d'un sous-objet et que vous souhaitez afficher la progression des sous-objets, transférez un pointeur vers l'objet Progress dans le paramètre _lpProgress_ vers la méthode. 
      
   3. Appelez [méthode imapiprogress::P rogress](imapiprogress-progress.md) et transmettez les valeurs suivantes pour les trois paramètres: 
      
     - Définissez le paramètre _ulValue_ sur la variable définie à l'étape 2 multipliée par l'objet actif. 
      
     - Définissez le paramètre _ulCount_ sur l'objet actif. 
      
     - Définissez le paramètre _ulTotal_ sur la variable définie à l'étape 1, le nombre total d'objets. 
    
Si l'indicateur MAPI_TOP_LEVEL n'est pas défini, procédez comme suit:
  
1. Appelez la méthode [méthode imapiprogress:: GetMin](imapiprogress-getmin.md) de l'objet de progression pour extraire la valeur minimale pour l'affichage. 
    
2. Appelez [méthode imapiprogress:: GetMax](imapiprogress-getmax.md) pour récupérer la valeur maximale de l'affichage. 
    
3. Définissez une variable égale au nombre total d'objets à traiter. 
    
4. Définissez une variable égale au résultat obtenu en soustrayant la valeur minimale de la valeur maximale, puis en divisant le nombre total d'objets.
    
5. Pour chaque objet à traiter, procédez comme suit:
    
   1. Si votre fournisseur affiche la progression des sous-objets, appelez **méthode imapiprogress:: SetLimits** et transmettez les valeurs suivantes pour les trois paramètres: 
      
     - Définissez le paramètre _lpulMin_ sur la valeur minimale plus l'élément actif moins 1 multiplié par la variable définie à l'étape 4. 
      
     - Définissez le paramètre _lpulMax_ sur la valeur minimale plus l'unité actuelle multipliée par la variable définie à l'étape 4. 
      
     - Définissez le paramètre _lpulFlags_ sur 0. 
      
   2. Exécutez le traitement qui doit être effectué sur cet objet. Si l'objet est un sous-objet et que votre fournisseur affiche la progression des sous-objets, transmettez un pointeur vers l'objet Progress dans le paramètre _lpProgress_ à la méthode. 
      
   3. Appelez [méthode imapiprogress::P rogress](imapiprogress-progress.md) et transmettez les valeurs suivantes pour les trois paramètres: 
      
     - Définissez le paramètre _ulValue_ sur variable définie à l'étape 2 multipliée par l'objet actif. 
      
     - Définissez le paramètre _ulCount_ sur 0. 
      
     - Définissez le paramètre _ulTotal_ sur 0. 
    
L'exemple de code suivant illustre la logique requise pour afficher la progression à tous les niveaux d'une opération qui copie le contenu d'un dossier contenant cinq sous-dossiers. 
  
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

