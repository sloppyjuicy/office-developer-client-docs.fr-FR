---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787256"
---
# <a name="sshortarray"></a>SShortArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau d’entiers non signés sont utilisées pour décrire une propriété de type PT_MV_SHORT.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **LPP** . 
    
 **LPP**
  
> Pointeur vers un tableau de valeurs de nombre entier non signé.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_SHORT et d’autres types de propriété, voir [Types de propriété](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

