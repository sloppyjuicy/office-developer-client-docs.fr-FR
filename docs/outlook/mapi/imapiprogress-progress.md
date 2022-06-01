---
title: IMAPIProgressProgress
description: IMAPIProgressProgress met à jour l’indicateur de progression avec un affichage de la progression à mesure qu’il est effectué vers la fin de l’opération.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
ms.openlocfilehash: 37789abad6830052e59f2bc3b293e3c4c4dc2486
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816828"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met à jour l’indicateur de progression avec un affichage de la progression à mesure qu’il est effectué vers la fin de l’opération. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Paramètres

 _ulValue_
  
> [in] Nombre qui indique le niveau de progression actuel (calculé à partir des paramètres  _ulCount_ et  _ulTotal_ ou des paramètres  _lpulMin_ et  _lpulMax_ de la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) ) entre la limite inférieure globale et la limite supérieure globale. 
    
 _ulCount_
  
> [in] Nombre qui indique l’élément actuellement traité par rapport au total.
    
 _ulTotal_
  
> [in] Nombre total d’éléments à traiter pendant l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’indicateur de progression a été correctement mis à jour.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le paramètre  _ulValue_ est égal à la valeur minimale globale uniquement au début de l’opération et à la valeur maximale globale uniquement à la fin de l’opération. 
  
Utilisez les paramètres  _ulCount_ et  _ulTotal_ , le cas échéant, pour afficher un message facultatif tel que « 5 éléments terminés sur 10 ». Si  _ulCount_ et  _ulTotal_ sont définis sur 0, décidez s’il faut modifier visuellement l’indicateur de progression. Certains fournisseurs de services définissent ces paramètres sur 0 pour indiquer qu’ils traitent un sous-objet dont la progression est surveillée par rapport à un objet parent. Dans ce cas, il est judicieux de modifier l’affichage uniquement lorsque l’objet parent signale la progression. Certains fournisseurs de services passent 0 pour ces paramètres à chaque fois. 
  
Pour plus d’informations sur la façon d’implémenter **Progress** et les autres méthodes [IMAPIProgress](imapiprogressiunknown.md) , consultez [Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les trois paramètres **d’IMAPIProgress::P rogress ne** sont pas tous requis. Le seul paramètre requis est  _ulValue_, un nombre qui indique le pourcentage de progression. Si l’indicateur MAPI_TOP_LEVEL est défini, vous pouvez également passer un nombre d’objets et un total d’objets. Certaines implémentations utilisent ces valeurs pour afficher une expression telle que « 5 éléments terminés sur 10 » avec l’indicateur de progression. 
  
Si vous copiez tous les messages d’un même dossier, définissez  _ulTotal_ sur le nombre total de messages copiés. Si vous copiez un dossier, définissez  _ulTotal_ sur le nombre de sous-dossiers dans le dossier. Si le dossier à copier ne contient aucun sous-dossier et uniquement des messages, définissez  _ulTotal_ sur 1. 
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::P rogress** pour mettre à jour la barre d’état MFCMAPI avec le pourcentage actuel de progression, calculé à partir  _d’uValue_ et des valeurs maximales et minimales actuelles. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

