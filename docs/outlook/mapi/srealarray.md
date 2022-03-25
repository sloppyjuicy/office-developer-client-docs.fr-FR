---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: Contient un tableau de valeurs flottantes utilisées pour décrire une propriété de type PT_MV_R4.
ms.openlocfilehash: 30922de70cc0dcc09a62c94a8e3ab1b89672de5d
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781844"
---
# <a name="srealarray"></a>SRealArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs flottantes utilisées pour décrire une propriété de type PT_MV_R4. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpflt** . 
    
 **lpflt**
  
> Pointeur vers un tableau de valeurs flottantes.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_R4 type de propriété, voir [Types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

