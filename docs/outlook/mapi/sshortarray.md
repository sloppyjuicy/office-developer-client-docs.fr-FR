---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: Contient un tableau de valeurs d’un nombre integer non signé qui sont utilisées pour décrire une propriété de type PT_MV_SHORT.
ms.openlocfilehash: cce5e5b870f3eb275bc1ea64885d262069ce9ae8
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455488"
---
# <a name="sshortarray"></a>SShortArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs d’un nombre integer non signé qui sont utilisées pour décrire une propriété de type PT_MV_SHORT.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpi** . 
    
 **lpi**
  
> Pointeur vers un tableau de valeurs d’un nombre integer non signé.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_SHORT types de propriétés et d’autres types de propriétés, voir [Types de propriétés](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

