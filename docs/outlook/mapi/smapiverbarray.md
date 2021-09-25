---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fe3bcec6e8e0c3148314bf97a8597e784c45aefe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609452"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SMAPIVerb](smapiverb.md) qui décrivent les verbes MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Macro associée :  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a>Members

 **cForms**
  
> Nombre de verbes dans le tableau.
    
 **aFormInfo**
  
> Tableau de verbes MAPI.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIVerbArray** est transmise en tant que paramètre dans la méthode [IMAPIFormInfo::CalcVerbSet.](imapiforminfo-calcverbset.md) 
  
## <a name="see-also"></a>Voir aussi



[SMAPIVerb](smapiverb.md)


[Structures MAPI](mapi-structures.md)

