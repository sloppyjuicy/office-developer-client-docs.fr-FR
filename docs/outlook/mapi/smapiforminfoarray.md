---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319172"
---
# <a name="smapiforminfoarray"></a>SMAPIFormInfoArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de pointeurs vers des objets d'informations de formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Macro connexe:  <br/> |[CbMAPIFormInfoArray](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a>Members

 **cForms**
  
> Nombre de pointeurs dans le tableau vers lequel pointe le membre **aFormInfo** . 
    
 **aFormInfo**
  
> Pointeur vers un tableau de pointeurs vers des objets d'informations de formulaire.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIFormInfoArray** est transmise en tant que paramètre dans les méthodes suivantes: 
  
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormMgr::SelectMultipleForms](imapiformmgr-selectmultipleforms.md)
    
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

