---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7dfec802ae869371a99c2f2354231c8d05211bb5
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631763"
---
# <a name="filetime"></a>FILETIME

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de date et d’heure 64 bits non signée pour un fichier. Cette valeur représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> 32 bits de bas ordre de la valeur de temps du fichier. 
    
 **dwHighDateTime**
  
> Ordre élevé de 32 bits de la valeur de temps du fichier.
    
## <a name="remarks"></a>Remarques

Une propriété de type PT_SYSTIME a une structure **FILETIME** pour sa valeur. Une telle propriété possède un type **de données FILETIME** pour le membre **Value** dans sa définition dans une structure [SPropValue](spropvalue.md) . 
  
La définition de la structure **FILETIME** se trouve dans la référence du programmeur _Win32_ et dans le fichier d’en-tête MAPI Mapidefs.h. MAPI définit la structure de manière conditionnelle pour s’assurer qu’elle est définie lorsque la définition Win32 n’est pas disponible. 
  
## <a name="see-also"></a>Consultez aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

