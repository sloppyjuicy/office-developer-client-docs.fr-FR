---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: Contient un tableau de doubles utilisé pour décrire une propriété de type PT_MV_DOUBLE pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 1fd8c3033c2a82e39fb88360ca633d05d6bc92f2
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762674"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de doubles utilisé pour décrire une propriété de type PT_MV_DOUBLE.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpdbl** . 
    
 **lpdbl**
  
> Pointeur vers un tableau de valeurs doubles.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_DOUBLE, voir [Liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

