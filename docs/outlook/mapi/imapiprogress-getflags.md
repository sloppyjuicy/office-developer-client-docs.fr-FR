---
title: IMAPIProgressGetFlags
description: IMAPIProgressGetFlags retourne les paramètres d’indicateur de l’objet progress pour le niveau d’opération sur lequel les informations de progression sont calculées.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
ms.openlocfilehash: e2c4c222a011e2252ae33546f0ea817549ffd80b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817724"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

**S’applique à** : Outlook 2013 | Outlook 2016
  
Retourne les paramètres d’indicateur de l’objet de progression pour le niveau d’opération sur lequel les informations de progression sont calculées.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [out] Masque de bits des indicateurs qui contrôle le niveau d’opération sur lequel les informations de progression sont calculées. L’indicateur suivant peut être retourné :

MAPI_TOP_LEVEL
  
> La progression est calculée pour l’objet de niveau supérieur, l’objet appelé par le client pour commencer l’opération. Par exemple, l’objet de niveau supérieur dans une opération de copie de dossier est le dossier qui est copié. Lorsque MAPI_TOP_LEVEL n’est pas défini, la progression est calculée pour un objet de niveau inférieur ou un sous-objet. Dans l’opération de copie de dossier, un objet de niveau inférieur est l’un des sous-dossiers du dossier en cours de copie.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La valeur des indicateurs a été retournée avec succès.

## <a name="remarks"></a>Remarques

MAPI permet aux fournisseurs de services de différencier les objets de niveau supérieur et les sous-objets avec l’indicateur MAPI_TOP_LEVEL afin que tous les objets impliqués dans une opération puissent utiliser la même implémentation [IMAPIProgress](imapiprogressiunknown.md) pour afficher la progression. Ainsi, l’affichage de l’indicateur se déroule sans problème dans une seule direction positive. La définition de l’indicateur MAPI_TOP_LEVEL détermine comment les fournisseurs de services définissent les autres paramètres dans les appels suivants à l’objet de progression.
  
La valeur retournée par **GetFlags** est définie initialement par l’implémenteur, puis par le fournisseur de services via un appel à la méthode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Initialisez toujours l’indicateur pour MAPI_TOP_LEVEL, puis comptez sur les fournisseurs de services pour l’effacer le cas échéant. Les fournisseurs de services peuvent effacer et réinitialiser l’indicateur en appelant la méthode **IMAPIProgress::SetLimits** . Pour plus d’informations sur l’implémentation de **GetFlags et des** autres méthodes **IMAPIProgress** , consultez [Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous affichez un indicateur de progression, effectuez votre premier appel à **IMAPIProgress::GetFlags**. La valeur retournée doit être MAPI_TOP_LEVEL, car toutes les implémentations initialisent le contenu du paramètre _lpulFlags_ à cette valeur. Pour plus d’informations sur la séquence d’appels à un objet de progression, consultez [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI utilise la méthode **IMAPIProgress::GetFlags** pour déterminer les indicateurs définis. Retourne MAPI_TOP_LEVEL sauf si des indicateurs ont été définis à l’aide de la méthode **IMAPIProgress::SetLimits** . |

## <a name="see-also"></a>Voir aussi

[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)  
[Affichage d’un indicateur de progression](how-to-display-a-progress-indicator.md)  
[Implémentation d’un indicateur de progression](implementing-a-progress-indicator.md)
