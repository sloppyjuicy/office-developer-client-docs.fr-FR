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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787212"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 **ulReserved**
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 **lpRes**
  
> Pointeur vers une structure [SRestriction](srestriction.md) décrivant la restriction être lié à l’opérateur **NOT** logique. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur la structure **SNotRestriction** , voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

