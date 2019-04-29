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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420065"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SMAPIFormProp](smapiformprop.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Macro connexe:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
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
  
>  Huit octets de remplissage utilisés pour garantir un alignement correct. 
    
 **aFormProp**
  
> Tableau de propriétés de formulaire.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIFormPropArray** est transmise en tant que paramètre aux méthodes suivantes: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Voir aussi



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Structures MAPI](mapi-structures.md)

