---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: Contient un tableau de pointeurs vers des chaînes de classe de message pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: a4bfdfae714ec495f73dfb3dd61dde75cad22a1d
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455649"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de pointeurs vers des chaînes de classe de message.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Macro associée :  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de pointeurs de chaîne de classe de message dans le tableau.
    
 **aMessageClass**
  
> Tableau de pointeurs vers des chaînes de classe de message.
    
## <a name="remarks"></a>Remarques

La structure **SMessageClassArray** est passée en tant que paramètre dans les méthodes suivantes : 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

