---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f8fc822d4b3d11b2b310e511d43da612ffcc32c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566562"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une erreur liée à une opération impliquant une propriété.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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
  
> Index dans un tableau de balises de propriétés.
    
 **ulPropTag**
  
> Balise de propriété de la propriété qui présente l’erreur.
    
 **scode**
  
> Valeur d’erreur décrivant le problème avec la propriété. Cette valeur peut être n’importe quelle valeur [MAPI SCODE.](scode.md) 
    
## <a name="remarks"></a>Remarques

Un tableau de structures **SPropProblem** est renvoyé à partir des méthodes suivantes : 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Une structure **SPropProblem** contient une valeur d’erreur **SCODE** qui résulte d’une opération de modification ou de suppression d’une propriété MAPI. 
  
Pour plus d’informations sur le fonctionnement de la structure **SPropProblem** avec les erreurs liées aux propriétés, voir [PROPRIÉTÉS nommées MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Structures MAPI](mapi-structures.md)

