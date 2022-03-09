---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
ms.openlocfilehash: f1443e630b69519c94d1ef700d11629aa2fc08b8
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380990"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un tableau des propriétés qu’un groupe de formulaires utilise.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Paramètres

 _pfrminfoarray_
  
> [in] Pointeur vers un tableau d’objets d’informations de formulaire qui identifient les formulaires pour lesquels renvoyer des propriétés.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le tableau de _propriétés dans le paramètre ppResults_ est renvoyé. Les indicateurs suivants peuvent être définies : 
    
FORMPROPSET_INTERSECTION 
  
> Le tableau renvoyé contient l’intersection des propriétés du formulaire.
    
FORMPROPSET_UNION 
  
> Le tableau renvoyé contient l’union des propriétés du formulaire.
    
MAPI_UNICODE 
  
> Les chaînes renvoyées dans le tableau sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _ppResults_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée, qui contient les propriétés que les formulaires utilisent. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::CalcFormPropSet** pour obtenir un tableau des propriétés utilisées par un groupe de formulaires. **CalcFormPropSet** prend une intersection ou une union des jeux de propriétés de ces formulaires, en fonction de l’indicateur définie dans le paramètre _ulFlags_ , et il renvoie une structure **SMAPIFormPropArray** qui contient le groupe de propriétés résultant. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si une visionneuse de formulaire passe l’MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes doivent être renvoyées sous forme de chaînes Unicode. Les fournisseurs de bibliothèques de formulaires qui ne prisent pas en charge les chaînes Unicode doivent MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé. 
  
## <a name="see-also"></a>Voir aussi



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

