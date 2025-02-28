---
title: HrSzFromEntryID
description: Cet article décrit la fonction HrSzFromEntryID, il fournit une syntaxe, des paramètres, une valeur de retour et des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
ms.openlocfilehash: 584d74cc2eb9f45941ccc8af3d13e742f82a19b5
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815813"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Encode un identificateur d’entrée dans une chaîne ASCII. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Paramètres

 _cb_
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par le paramètre  _pentry_ . 
    
 _pentry_
  
> [in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée à encoder. 
    
 _Zsp_
  
> [out] Pointeur vers la chaîne ASCII retournée.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les fonctions [HrEntryIDFromSz](hrentryidfromsz.md) et **HrSzFromEntryID fournissent** une conversion entre les formats de chaîne et binaire des identificateurs d’entrée. Avec MAPI, vous devez utiliser des structures avec des données binaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La fonction **HrSzFromEntryID** alloue de la mémoire pour la chaîne ASCII à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

