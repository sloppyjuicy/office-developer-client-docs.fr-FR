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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573284"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une erreur qui sont associées à une opération impliquant une propriété.
  
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
  
> Un index dans un tableau de balises de propriété.
    
 **ulPropTag**
  
> Balise de propriété pour la propriété qui comporte l’erreur.
    
 **SCODE**
  
> Valeur d’erreur décrivant le problème avec la propriété. Cette valeur peut être n’importe quelle valeur MAPI [SCODE](scode.md) . 
    
## <a name="remarks"></a>Remarques

Un tableau de structures **SPropProblem** est renvoyé à partir des méthodes suivantes : 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
Une structure **SPropProblem** contient une valeur d’erreur **SCODE** qui se traduit par une opération que vous tentez de modifier ou supprimer une propriété MAPI. 
  
Pour plus d’informations sur le fonctionne de la structure **SPropProblem** avec des erreurs liées aux propriétés, voir [Les propriétés MAPI nommée](mapi-named-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Structures MAPI](mapi-structures.md)

