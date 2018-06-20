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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783785"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**S’applique à**: Outlook 
  
Renvoie un tableau des propriétés qui utilise un groupe de formulaires.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Paramètres

 _pfrminfoarray_
  
> [in] Pointeur vers un tableau d’objets d’informations de formulaire qui identifient les formulaires pour laquelle retourner les propriétés.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le tableau de propriétés dans le paramètre _ppResults_ est renvoyé. Les indicateurs suivants peuvent être définis : 
    
FORMPROPSET_INTERSECTION 
  
> La matrice renvoyée contient l’intersection des propriétés du formulaire.
    
FORMPROPSET_UNION 
  
> Le tableau renvoyé contient l’union de propriétés du formulaire.
    
MAPI_UNICODE 
  
> Les chaînes renvoyées dans le tableau sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _ppResults_
  
> [out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée, qui contient les propriétés qui utilisent les formulaires. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::CalcFormPropSet** pour obtenir un tableau des propriétés qui utilise un groupe de formulaires. **CalcFormPropSet** accepte soit une intersection ou une union de propriété des formulaires définit, en fonction de l’indicateur défini dans le paramètre _ulFlags_ et elle renvoie une structure **SMAPIFormPropArray** qui contient le groupe résultant de Propriétés. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si une visionneuse de formulaire transmet l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes doivent être retournés en tant que chaînes Unicode. Fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé. 
  
## <a name="see-also"></a>Voir aussi



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

