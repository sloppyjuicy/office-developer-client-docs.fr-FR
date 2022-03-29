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
description: Décrit une erreur liée à une opération impliquant une propriété pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 5faab803c93b85b5efb7b67f0775e49536936d84
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455201"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une erreur liée à une opération impliquant une propriété.
  
|Propriété |Valeur |
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
  
> Valeur d’erreur décrivant le problème avec la propriété. Cette valeur peut être n’importe quelle valeur [MAPI SCODE](scode.md) . 
    
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
  
Pour plus d’informations sur le fonctionnement de **la structure SPropProblem** avec les erreurs liées aux propriétés, voir [PROPRIÉTÉS nommées MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[Structures MAPI](mapi-structures.md)

