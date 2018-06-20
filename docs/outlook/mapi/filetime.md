---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783309"
---
# <a name="filetime"></a>FILETIME

  
  
**S’applique à**: Outlook 
  
Contient une date de 64 bits non signé et d’une valeur d’heure d’un fichier. Cette valeur représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Membres

 **dwLowDateTime**
  
> Valeur de temps 32 bits de poids faible du fichier. 
    
 **FILETIME**
  
> Ordre haut 32 bits de la valeur d’heure de fichier.
    
## <a name="remarks"></a>Remarques

Une propriété de type PT_SYSTIME possède une structure **FILETIME** pour sa valeur. Ces propriétés a un type de données **FILETIME** pour le membre de la **valeur** de sa définition dans une structure [SPropValue](spropvalue.md) . 
  
La définition de la structure **FILETIME** est dans la _référence du programmeur Win32_ et dans le fichier d’en-tête Mapidefs.h MAPI. MAPI définit la structure conditionnelle pour vous assurer qu’elle est définie lorsque la définition de Win32 n’est pas disponible. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

