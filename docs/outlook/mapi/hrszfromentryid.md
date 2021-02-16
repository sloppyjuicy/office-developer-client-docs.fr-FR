---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411553"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Encode un identificateur d’entrée dans une chaîne ASCII. 
  
|||
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
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par le paramètre _pentry._ 
    
 _pentry_
  
> [in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée à coder. 
    
 _psz_
  
> [out] Pointeur vers la chaîne ASCII renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les [fonctions HrEntryIDFromSz](hrentryidfromsz.md) et **HrSzFromEntryID** permettent de convertir les formats de chaîne et binaires des identificateurs d’entrée. Avec MAPI, vous devez utiliser des structures avec des données binaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La **fonction HrSzFromEntryID** alloue de la mémoire pour la chaîne ASCII à l’aide de la [fonction MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  

