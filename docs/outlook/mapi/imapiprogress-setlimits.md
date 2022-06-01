---
title: IMAPIProgressSetLimits
description: IMAPIProgressSetLimits définit les limites du nombre d’éléments de l’opération et les indicateurs qui contrôlent la façon dont les informations de progression sont calculées.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
ms.openlocfilehash: 68588bf9cb4cacc41a376e4698c8505f1d3ca25a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817073"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

**S’applique à** : Outlook 2013 | Outlook 2016
  
Définit les limites inférieure et supérieure pour le nombre d’éléments de l’opération, ainsi que les indicateurs qui contrôlent la façon dont les informations de progression sont calculées pour l’opération.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulMin_
  
> [in] Pointeur vers une variable qui contient la limite inférieure des éléments de l’opération.

 _lpulMax_
  
> [in] Pointeur vers une variable qui contient la limite supérieure des éléments de l’opération.

 _lpulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le niveau d’opération sur lequel les informations de progression sont calculées. L’indicateur suivant peut être défini :

MAPI_TOP_LEVEL
  
> Utilise les valeurs des paramètres _ulCount_ et _ulTotal_ de la méthode [IMAPIProgress::P rogress](imapiprogress-progress.md), qui indiquent l’élément actuellement traité et le total des éléments, respectivement, pour incrémenter la progression de l’opération. Lorsque cet indicateur est défini, les valeurs des limites globales inférieures et supérieures doivent être définies.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

## <a name="remarks"></a>Remarques

Les fournisseurs de services appellent la méthode **IMAPIProgress::SetLimits** pour définir ou effacer l’indicateur MAPI_TOP_LEVEL et définir des valeurs minimales et maximales locales et globales. La valeur du paramètre d’indicateur détermine si l’objet de progression comprend les valeurs minimales et maximales locales ou globales. Lorsque l’indicateur MAPI_TOP_LEVEL est défini, ces valeurs sont considérées comme globales et sont utilisées pour calculer la progression de l’ensemble de l’opération. Les objets progress initialisent la valeur minimale globale à 1 et la valeur maximale globale à 1 000.
  
Lorsque MAPI_TOP_LEVEL n’est pas défini, les valeurs minimales et maximales sont considérées comme locales et les fournisseurs les utilisent en interne pour afficher la progression des sous-objets de niveau inférieur. Les objets progress enregistrent les valeurs minimale et maximale locales uniquement afin qu’elles puissent être retournées aux fournisseurs lorsque les méthodes [IMAPIProgress::GetMin](imapiprogress-getmin.md) et [IMAPIProgress::GetMax](imapiprogress-getmax.md) sont appelées.
  
Pour plus d’informations sur la façon d’implémenter **SetLimits** et les autres méthodes [IMAPIProgress](imapiprogressiunknown.md) , consultez [Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
Pour plus d’informations sur la méthode et le moment opportun pour appeler un objet de progression, reportez-vous à [Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::SetLimits** pour définir les limites maximales et minimales et les indicateurs pour l’objet de progression. |

## <a name="see-also"></a>Voir aussi

[IMAPIProgress::GetMax](imapiprogress-getmax.md)
 [IMAPIProgress::GetMin](imapiprogress-getmin.md)  
[IMAPIProgress::Progress](imapiprogress-progress.md)  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)
