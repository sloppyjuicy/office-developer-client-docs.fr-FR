---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: Contient un tableau de valeurs de chaîne qui sont utilisées pour décrire une propriété de type PT_MV_STRING8.
ms.openlocfilehash: 76c79896abd5c4098062699dcbe40daf8ad76155
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762822"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs de chaîne qui sont utilisées pour décrire une propriété de type PT_MV_STRING8.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par le **membre lppszA** . 
    
 **lppszA**
  
> Pointeur vers un tableau de chaînes de caractères de 8 bits de fin null.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_STRING8, voir [Liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

