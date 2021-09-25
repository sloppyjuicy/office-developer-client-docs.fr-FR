---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e88762457df923b88c22bc21845052f39c2fe051
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571814"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaires.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le tableau de propriétés dans le  _paramètre ppResults_ est renvoyé. Les indicateurs suivants peuvent être définies : 
    
FORMPROPSET_INTERSECTION 
  
> Le tableau renvoyé contient l’intersection des propriétés des formulaires.
    
FORMPROPSET_UNION 
  
> Le tableau renvoyé contient l’union des propriétés des formulaires.
    
MAPI_UNICODE 
  
> Les chaînes renvoyées dans le tableau sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _ppResults_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée. Cette structure contient toutes les propriétés utilisées par les formulaires installés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormContainer::CalcFormPropSet** pour obtenir un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaires. **IMAPIFormContainer::CalcFormPropSet** fonctionne comme la méthode [IMAPIFormMgr::CalcFormPropSet,](imapiformmgr-calcformpropset.md) sauf qu’elle fonctionne sur chaque formulaire enregistré dans un conteneur particulier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de bibliothèques de formulaires qui ne prisent pas en charge les chaînes Unicode doivent MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **IMAPIFormContainer::CalcFormPropSet** prend une intersection ou une union des jeux de propriétés des formulaires, en fonction de l’indicateur définie dans le paramètre  _ulFlags,_ et elle renvoie une structure **SMAPIFormPropArray** qui contient le groupe de propriétés résultant. 
  
Si un client passe l’MAPI_UNICODE dans  _ulFlags,_ toutes les chaînes renvoyées sont Unicode.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

