---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412694"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de pointeurs vers des chaînes de classe de message.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Macro connexe:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
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

La structure **SMessageClassArray** est transmise en tant que paramètre dans les méthodes suivantes: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

