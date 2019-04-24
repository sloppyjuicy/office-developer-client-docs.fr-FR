---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357476"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SMAPIVerb](smapiverb.md) qui décrivent les verbes MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Macro connexe:  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
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

La structure **SMAPIVerbArray** est transmise sous la forme d'un paramètre dans la méthode [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>Voir aussi



[SMAPIVerb](smapiverb.md)


[Structures MAPI](mapi-structures.md)

