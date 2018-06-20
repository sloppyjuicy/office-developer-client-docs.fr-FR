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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787202"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

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

