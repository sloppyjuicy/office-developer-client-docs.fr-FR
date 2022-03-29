---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: Contient un tableau de structures SMAPIFormProp pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 774fa4a4449f7d7f8d1481f650b57d7129428bee
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456265"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SMAPIFormProp](smapiformprop.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Macro associée :  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
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
  
> Nombre de propriétés nommées dans le tableau dans le **membre aFormProp** . 
    
 **ulPad**
  
>  Huit octets de remplissage utilisés pour garantir un alignement correct. 
    
 **aFormProp**
  
> Tableau de propriétés de formulaire.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIFormPropArray** est transmise en tant que paramètre aux méthodes suivantes : 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Voir aussi



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Structures MAPI](mapi-structures.md)

