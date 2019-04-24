---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342083"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un tableau des propriétés utilisées par un groupe de formulaires.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Paramètres

 _pfrminfoarray_
  
> dans Pointeur vers un tableau d'objets d'informations de formulaire qui identifient les formulaires pour lesquels renvoyer des propriétés.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont le tableau de propriétés dans le paramètre _ppResults_ est renvoyé. Les indicateurs suivants peuvent être définis: 
    
FORMPROPSET_INTERSECTION 
  
> Le tableau renvoyé contient l'intersection des propriétés du formulaire.
    
FORMPROPSET_UNION 
  
> Le tableau renvoyé contient l'Union des propriétés du formulaire.
    
MAPI_UNICODE 
  
> Les chaînes renvoyées dans le tableau sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _ppResults_
  
> remarquer Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée, qui contient les propriétés utilisées par les formulaires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: CalcFormPropSet** pour obtenir un tableau des propriétés utilisées par un groupe de formulaires. **CalcFormPropSet** prend une intersection ou une Union des jeux de propriétés de ces formulaires, en fonction de l'indicateur défini dans le paramètre _ulFlags_ , et renvoie une structure **SMAPIFormPropArray** qui contient le groupe résultant de Propriétés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si une visionneuse de formulaires transmet l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes doivent être renvoyées en tant que chaînes Unicode. Les fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est transmis. 
  
## <a name="see-also"></a>Voir aussi



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

