---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421465"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les limites inférieure et supérieure du nombre d’éléments dans l’opération, ainsi que les indicateurs qui contrôlent la façon dont les informations de progression sont calculées pour l’opération.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulMin_
  
> [in] Pointeur vers une variable qui contient la limite inférieure d’éléments dans l’opération.
    
 _lpulMax_
  
> [in] Pointeur vers une variable qui contient la limite supérieure des éléments de l’opération.
    
 _lpulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le niveau de fonctionnement sur lequel les informations de progression sont calculées. L’indicateur suivant peut être définie :
    
MAPI_TOP_LEVEL 
  
> Utilise les valeurs des paramètres _ulCount_ et _ulTotal_ de la méthode [IMAPIProgress::P rogress,](imapiprogress-progress.md) qui indiquent respectivement l’élément actuellement traitée et le nombre total d’éléments pour incrémenter l’avancement de l’opération. Lorsque cet indicateur est définie, les valeurs des limites inférieures et supérieures globales doivent être définies. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de services appellent la méthode **IMAPIProgress::SetLimits** pour définir ou effacer l’indicateur MAPI_TOP_LEVEL et pour définir les valeurs minimales et maximales locales et globales. La valeur du paramètre d’indicateur affecte si l’objet de progression comprend les valeurs minimales et maximales à être locales ou globales. Lorsque l MAPI_TOP_LEVEL est définie, ces valeurs sont considérées comme globales et sont utilisées pour calculer la progression de l’ensemble de l’opération. Les objets de progression initialisent la valeur minimale globale sur 1 et la valeur maximale globale à 1 000. 
  
Lorsque MAPI_TOP_LEVEL n’est pas définie, les valeurs minimale et maximale sont considérées comme locales et les fournisseurs les utilisent en interne pour afficher la progression des sous-objets de niveau inférieur. Les objets de progression enregistrent les valeurs minimale et maximale locales uniquement afin de pouvoir être renvoyés aux fournisseurs lorsque les méthodes [IMAPIProgress::GetMin](imapiprogress-getmin.md) et [IMAPIProgress::GetMax](imapiprogress-getmax.md) sont appelées. 
  
Pour plus d’informations sur l’implémentation de **SetLimits** et des autres méthodes [IMAPIProgress,](imapiprogressiunknown.md) voir [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::SetLimits** pour définir les limites maximales et minimales et les indicateurs de l’objet de progression.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)
  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)

