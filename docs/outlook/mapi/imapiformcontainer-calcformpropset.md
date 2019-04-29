---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414913"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaire.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont le tableau de propriétés dans le paramètre _ppResults_ est renvoyé. Les indicateurs suivants peuvent être définis: 
    
FORMPROPSET_INTERSECTION 
  
> Le tableau renvoyé contient l'intersection des propriétés des formulaires.
    
FORMPROPSET_UNION 
  
> Le tableau renvoyé contient l'Union des propriétés des formulaires.
    
MAPI_UNICODE 
  
> Les chaînes renvoyées dans le tableau sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _ppResults_
  
> remarquer Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée. Cette structure contient toutes les propriétés utilisées par les formulaires installés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormContainer:: CalcFormPropSet** pour obtenir un tableau de propriétés utilisées par tous les formulaires installés dans un conteneur de formulaire. **IMAPIFormContainer:: CalcFormPropSet** fonctionne comme la méthode [IMAPIFormMgr:: CalcFormPropSet](imapiformmgr-calcformpropset.md) , à la différence qu'elle fonctionne sur tous les formulaires inscrits dans un conteneur particulier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est transmis.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **IMAPIFormContainer:: CalcFormPropSet** accepte une intersection ou une Union des jeux de propriétés des formulaires, en fonction de l'indicateur défini dans le paramètre _ulFlags_ , et renvoie une structure **SMAPIFormPropArray** qui contient le Groupe de propriétés obtenu. 
  
Si un client transmet l'indicateur MAPI_UNICODE dans _ulFlags_, toutes les chaînes renvoyées sont au format Unicode.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

