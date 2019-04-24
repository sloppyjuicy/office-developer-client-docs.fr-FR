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
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334810"
---
# <a name="filetime"></a>FILETIME

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de date et d'heure 64 bits non signée pour un fichier. Cette valeur représente le nombre d'unités de 100 nanosecondes depuis le 1er janvier 1601. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> Ordre bas 32 bits de la valeur de l'heure du fichier. 
    
 **dwHighDateTime**
  
> Ordre 32 bits de poids fort de la valeur de l'heure du fichier.
    
## <a name="remarks"></a>Remarques

Une propriété de type PT_SYSTIME a une structure **fileTime** pour sa valeur. Une telle propriété a un type de données **fileTime** pour le membre de **valeur** dans sa définition dans une structure [SPropValue](spropvalue.md) . 
  
La définition de la structure **fileTime** se trouve dans le _Guide de référence du programmeur Win32_ et dans le fichier d'en-tête MAPI Mapidefs. h. MAPI définit la structure de façon conditionnelle pour s'assurer qu'elle est définie lorsque la définition Win32 n'est pas disponible. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

