---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407773"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une erreur liée à une opération impliquant une propriété.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>Members

 **ulIndex**
  
> Index dans un tableau de balises de propriété.
    
 **ulPropTag**
  
> Balise de propriété de la propriété présentant l'erreur.
    
 **SCODE**
  
> Valeur d'erreur décrivant le problème lié à la propriété. Cette valeur peut être n'importe quelle valeur [SCODE](scode.md) MAPI. 
    
## <a name="remarks"></a>Remarques

Un tableau de structures **SPropProblem** est renvoyé à partir des méthodes suivantes: 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Une structure **SPropProblem** contient une valeur d'erreur **SCODE** qui résulte d'une opération tentant de modifier ou de supprimer une propriété MAPI. 
  
Pour plus d'informations sur la façon dont la structure **SPropProblem** fonctionne avec les erreurs liées aux propriétés, consultez la rubrique [MAPI named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Structures MAPI](mapi-structures.md)

