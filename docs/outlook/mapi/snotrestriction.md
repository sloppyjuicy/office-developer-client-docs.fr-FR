---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e49b721bc50465c2b0e3191cc8a57d353fceeb17
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566583"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction **NOT,** qui est utilisée pour appliquer une opération **LOGIQUE NOT** à une restriction. 
  
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
  
> Pointeur vers une structure [SRestriction](srestriction.md) décrivant la restriction à joindre à l’opérateur **logique NOT.** 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur la structure **SNotRestriction,** voir [À propos des restrictions.](about-restrictions.md) 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

