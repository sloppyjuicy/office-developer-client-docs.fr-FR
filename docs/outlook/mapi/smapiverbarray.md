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
description: Contient un tableau de structures SMAPIVerb qui décrivent les verbes MAPI pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 1637144ca444397ac641428553fe5e7012b1cbbb
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455502"
---
# <a name="smapiverbarray"></a>SMAPIVerbArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SMAPIVerb](smapiverb.md) qui décrivent les verbes MAPI. 
  
|Propriété |Valeur |
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

La structure **SMAPIVerbArray** est passée en tant que paramètre dans la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) . 
  
## <a name="see-also"></a>Voir aussi



[SMAPIVerb](smapiverb.md)


[Structures MAPI](mapi-structures.md)

