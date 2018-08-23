---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579311"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SMAPIFormProp](smapiformprop.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Macro connexe :  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a>Members

 **cProps**
  
> Nombre de propriétés nommées dans le tableau dans le membre **aFormProp** . 
    
 **ulPad**
  
>  Huit octets de remplissage utilisé pour garantir l’alignement correct. 
    
 **aFormProp**
  
> Tableau de propriétés du formulaire.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIFormPropArray** est transmise en tant que paramètre aux méthodes suivantes : 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Voir aussi



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Structures MAPI](mapi-structures.md)

