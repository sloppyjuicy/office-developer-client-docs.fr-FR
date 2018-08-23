---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575062"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une restriction **pas** , qui est utilisée pour appliquer une opération **NOT** logique à une restriction. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Members

 **ulReserved**
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 **lpRes**
  
> Pointeur vers une structure [SRestriction](srestriction.md) décrivant la restriction être lié à l’opérateur **NOT** logique. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur la structure **SNotRestriction** , voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

