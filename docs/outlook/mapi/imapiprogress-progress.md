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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3fc72f008d1c2610de3c74762aabc6231dabbfbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589055"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Met à jour l’indicateur de progression avec un affichage de la progression qu’elle est réalisée vers la fin de l’opération. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Paramètres

 _ulValue_
  
> [in] Un nombre qui indique le niveau actuel de l’avancement (calculée à partir des paramètres _ulCount_ et _ulTotal_ ou à partir des paramètres de la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) _lpulMin_ et _lpulMax_ ) entre le modèle global limite inférieure et la limite supérieure globale. 
    
 _ulCount_
  
> [in] Nombre qui indique l’élément actuellement traitée par rapport au total.
    
 _ulTotal_
  
> [in] Nombre total d’éléments à être traités au cours de l’opération.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’indicateur de progression a été correctement mis à jour.
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Le paramètre _ulValue_ est égal à la valeur minimale globale uniquement au début de l’opération et à la valeur maximale globale uniquement à la fin de l’opération. 
  
Utiliser les paramètres _ulCount_ et _ulTotal_ , le cas échéant afficher un message facultatif, tel que « 5 éléments terminé sur 10 ». Si _ulCount_ et _ulTotal_ sont définies à 0, décider s’il faut modifier visuellement l’indicateur de progression. Certains fournisseurs de services de définissent ces paramètres à 0 pour indiquer qu’ils sont traitement un sous-objet dont la progression est surveillée par rapport à un objet parent. Dans ce cas, il est logique de modifier l’affichage uniquement lorsque l’objet parent signale la progression. Certains fournisseurs de services passez 0 pour ces paramètres à chaque fois. 
  
Pour plus d’informations sur l’implémentation de **progression** et les autres méthodes [IMAPIProgress](imapiprogressiunknown.md) , consultez [l’implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notes aux appelants

Trois pas tous les paramètres **IMAPIProgress::Progress** sont requis. Le seul paramètre requis est un _objet ulValue_, un nombre qui indique le pourcentage d’avancement. Si l’indicateur MAPI_TOP_LEVEL est défini, vous pouvez également passer un nombre d’objets et un total de l’objet. Certaines implémentations utilisent ces valeurs pour afficher une phrase tel que « 5 éléments terminé sur 10 » avec l’indicateur de progression. 
  
Si vous copiez tous les messages dans un dossier unique, définissez _ulTotal_ et le nombre total de messages en cours de copie. Si vous copiez un dossier, définissez _ulTotal_ au nombre de sous-dossiers dans le dossier. Si le dossier à copier ne contient aucun uniquement les messages et les sous-dossiers, _ulTotal_ la valeur 1. 
  
Pour plus d’informations sur la façon et le moment pour effectuer des appels à un objet de l’avancement, voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::Progress  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::Progress** pour mettre à jour de la barre d’état MFCMAPI avec le pourcentage d’avancement, calculée à partir de _uValue_ et les valeurs maximales et minimales en cours.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Afficher un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

