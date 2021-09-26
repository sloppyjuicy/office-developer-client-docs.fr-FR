---
title: IMAPIProgressProgress
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 92da3cc185fec19fc8cb1e7e7089ba029cd95cb3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620960"
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
  
> [in] Nombre qui indique le niveau actuel de progression (calculé à partir des paramètres  _ulCount_ et  _ulTotal_ ou des paramètres  _lpulMin_ et  _lpulMax_ de la méthode [IMAPIProgress::SetLimits)](imapiprogress-setlimits.md) entre la limite inférieure globale et la limite supérieure globale. 
    
 _ulCount_
  
> [in] Nombre qui indique l’élément actuellement traitée par rapport au total.
    
 _ulTotal_
  
> [in] Nombre total d’éléments à traiter pendant l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’indicateur de progression a été mis à jour avec succès.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le  _paramètre ulValue_ sera égal à la valeur minimale globale uniquement au début de l’opération et à la valeur maximale globale uniquement à la fin de l’opération. 
  
Utilisez les  _paramètres ulCount_ et  _ulTotal,_ si disponible, pour afficher un message facultatif tel que « 5 éléments terminés sur 10 ». Si  _ulCount et_  _ulTotal_ sont définies sur 0, décidez s’il faut modifier visuellement l’indicateur de progression. Certains fournisseurs de services définissent ces paramètres sur 0 pour indiquer qu’ils traitent un sous-objet dont la progression est surveillée par rapport à un objet parent. Dans ce cas, il est logique de modifier l’affichage uniquement lorsque l’objet parent signale la progression. Certains fournisseurs de services passent 0 pour ces paramètres à chaque fois. 
  
Pour plus d’informations sur l’implémentation de **Progress** et des autres méthodes [IMAPIProgress,](imapiprogressiunknown.md) voir [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les trois paramètres de **IMAPIProgress::P rogress** ne sont pas obligatoires. Le seul paramètre requis est  _ulValue_, un nombre qui indique le pourcentage de progression. Si l MAPI_TOP_LEVEL est définie, vous pouvez également transmettre un nombre d’objets et un total d’objets. Certaines implémentations utilisent ces valeurs pour afficher une expression telle que « 5 éléments terminés sur 10 » avec l’indicateur de progression. 
  
Si vous copiez tous les messages dans un dossier unique, définissez  _ulTotal_ sur le nombre total de messages en cours de copie. Si vous copiez un dossier, définissez  _ulTotal_ sur le nombre de sous-dossiers du dossier. Si le dossier à copier ne contient pas de sous-dossiers et uniquement de messages, définissez  _ulTotal_ sur 1. 
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::P rogress** pour mettre à jour la barre d’état MFCMAPI avec le pourcentage actuel de progression, calculé à partir  _d’uValue_ et des valeurs maximales et minimales actuelles.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

