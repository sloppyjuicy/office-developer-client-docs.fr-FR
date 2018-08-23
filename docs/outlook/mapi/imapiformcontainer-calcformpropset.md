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
ms.openlocfilehash: 9c6a6d210230fc305aef46371c22f67b3d445a81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576581"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie un tableau de propriétés utilisées par tous les formulaires installés dans un conteneur de formulaire.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le tableau de propriétés dans le paramètre _ppResults_ est renvoyé. Les indicateurs suivants peuvent être définis : 
    
FORMPROPSET_INTERSECTION 
  
> Le tableau renvoyé contient l’intersection des propriétés des formulaires.
    
FORMPROPSET_UNION 
  
> Le tableau renvoyé contient l’union des propriétés des formulaires.
    
MAPI_UNICODE 
  
> Les chaînes renvoyées dans le tableau sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _ppResults_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) retournée. Cette structure contient toutes les propriétés utilisées par les formulaires installés. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

Applications clientes appellent la méthode **IMAPIFormContainer::CalcFormPropSet** pour obtenir un tableau de propriétés utilisés par tous les formulaires installés dans un conteneur de formulaire. **IMAPIFormContainer::CalcFormPropSet** fonctionne comme la méthode [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) , sauf qu’elle fonctionne dans tous les formulaires enregistrés dans un conteneur spécifique. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé.
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **IMAPIFormContainer::CalcFormPropSet** accepte une intersection ou une union des jeux de propriétés des formulaires, en fonction de l’indicateur défini dans le paramètre _ulFlags_ , et elle renvoie une structure **SMAPIFormPropArray** qui contient la groupe résultant des propriétés. 
  
Si un client passe l’indicateur MAPI_UNICODE _ulFlags_, toutes les chaînes renvoyées sont en Unicode.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

