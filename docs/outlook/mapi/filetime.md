---
title: FILETIME
description: Décrit FILETIME et fournit une syntaxe, des membres et des remarques supplémentaires.
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
ms.openlocfilehash: 432f96666db939e4f215e56c85fb6633fa10749e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816660"
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
  
> Ordre faible de 32 bits de la valeur d’heure du fichier. 
    
 **dwHighDateTime**
  
> Ordre élevé de 32 bits de la valeur d’heure du fichier.
    
## <a name="remarks"></a>Remarques

Une propriété de type PT_SYSTIME a une structure **FILETIME** pour sa valeur. Cette propriété a un type de données **FILETIME** pour le membre **Value** dans sa définition dans une structure [SPropValue](spropvalue.md) . 
  
La définition de la structure **FILETIME** se trouve dans la _référence du programmeur Win32_ et dans le fichier d’en-tête MAPI Mapidefs.h. MAPI définit la structure de manière conditionnelle pour s’assurer qu’elle est définie lorsque la définition Win32 n’est pas disponible. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

