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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 01563e3655d42abc62ea88a12f2878e5d81129d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787221"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de pointeurs vers des chaînes de classe de message.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Macro connexe :  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de pointeurs de chaîne de classe de message dans le tableau.
    
 **aMessageClass**
  
> Tableau de pointeurs vers des chaînes de classe de message.
    
## <a name="remarks"></a>Remarques

La structure **SMessageClassArray** est transmise en tant que paramètre dans les méthodes suivantes : 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

