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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787218"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 **cForms**
  
> Nombre de verbes dans le tableau.
    
 **aFormInfo**
  
> Tableau des verbes MAPI.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIVerbArray** est transmise en tant que paramètre dans la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>Voir aussi



[SMAPIVerb](smapiverb.md)


[Structures MAPI](mapi-structures.md)

