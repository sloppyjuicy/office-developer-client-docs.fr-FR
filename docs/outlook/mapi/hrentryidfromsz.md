---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1422a8f6568c210c2d4416a58f625cc701ca3616
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571947"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recrée un identificateur d’entrée à partir de son codage ASCII. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Paramètres

 _sz_
  
> [in] Pointeur vers la chaîne ASCII à partir de laquelle créer un identificateur d’entrée. 
    
 _pcb_
  
> [out] Pointeur vers la taille, en octets, de l’identificateur d’entrée pointé par le _paramètre ppentry._ 
    
 _ppentry_
  
> [out] Pointeur vers un pointeur vers la structure [ENTRYID](entryid.md) renvoyée qui contient le nouvel identificateur d’entrée. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La recréation a réussi.
    
MAPI_E_INVALID_ENTRYID
  
> L’ID d’entrée n’était pas valide.
    
## <a name="remarks"></a>Remarques

Les **fonctions HrEntryIDFromSz** et [HrSzFromEntryID](hrszfromentryid.md) permettent de convertir les formats de chaîne et binaires des identificateurs d’entrée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La **fonction HrEntryIDFromSz** alloue de la mémoire pour la chaîne ASCII à l’aide de la [fonction MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  

