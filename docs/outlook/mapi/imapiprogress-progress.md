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
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met à jour l'indicateur de progression avec un affichage de la progression au fur et à mesure de l'exécution de l'opération. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Paramètres

 _Objet_
  
> dans Nombre qui indique le niveau actuel de progression (calculé à partir des paramètres _ulCount_ et _ulTotal_ ou à partir des paramètres _lpulMin_ et _LpulMax_ de la méthode [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md) ) entre le Global limite inférieure et limite supérieure globale. 
    
 _ulCount_
  
> dans Nombre indiquant l'élément actuellement traité par rapport au total.
    
 _ulTotal_
  
> dans Nombre total d'éléments à traiter au cours de l'opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'indicateur de progression a été mis à jour avec succès.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le paramètre _ulValue_ est égal à la valeur minimale globale uniquement au début de l'opération et à la valeur maximale globale uniquement à la fin de l'opération. 
  
Utilisez les paramètres _ulCount_ et _ulTotal_ , s'ils sont disponibles, pour afficher un message facultatif, par exemple, «5 éléments terminés sur 10». Si _ulCount_ et _ulTotal_ sont définis sur 0, déterminez si l'indicateur de progression doit être modifié visuellement. Certains fournisseurs de services définissent ces paramètres sur 0 pour indiquer qu'ils traitent un sous-objet dont la progression est contrôlée par rapport à un objet parent. Dans ce cas, il est logique de modifier l'affichage uniquement lorsque l'objet parent indique la progression. Certains fournisseurs de services transfèrent 0 pour ces paramètres à chaque fois. 
  
Pour plus d'informations sur la façon d'implémenter la **progression** et les autres méthodes [méthode imapiprogress](imapiprogressiunknown.md) , consultez la rubrique [implémentation d'un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les trois paramètres de **méthode imapiprogress::P rogress** sont tous obligatoires. Le seul paramètre obligatoire est _ulValue_, un nombre qui indique le pourcentage d'avancement. Si l'indicateur MAPI_TOP_LEVEL est défini, vous pouvez également transmettre un nombre d'objets et un total d'objets. Certaines implémentations utilisent ces valeurs pour afficher une phrase telle que «5 éléments terminés sur 10» avec l'indicateur de progression. 
  
Si vous copiez tous les messages dans un seul dossier, définissez _ulTotal_ sur le nombre total de messages en cours de copie. Si vous copiez un dossier, définissez _ulTotal_ sur le nombre de sous-dossiers dans le dossier. Si le dossier à copier ne contient pas de sous-dossiers ni de messages, affectez la valeur 1 à _ulTotal_ . 
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI utilise la méthode **méthode imapiprogress::P rogress** pour mettre à jour la barre d'état de MFCMAPI avec le pourcentage d'avancement actuel, calculé à partir de _uValue_ et les valeurs maximale et minimale actuelles.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

