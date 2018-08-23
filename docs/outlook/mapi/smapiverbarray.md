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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7a2911779e5f9edb8c0bba7c3476a74ce410477c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569462"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SMAPIVerb](smapiverb.md) qui décrivent les verbes MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Macro connexe :  <br/> |[CbMAPIVerbArray](cbmapiverbarray.md) <br/> |
   
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
  
> Tableau des verbes MAPI.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIVerbArray** est transmise en tant que paramètre dans la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>Voir aussi



[SMAPIVerb](smapiverb.md)


[Structures MAPI](mapi-structures.md)

