---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783543"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**S’applique à**: Outlook 
  
Recrée un identificateur d’entrée à partir de l’encodage ASCII. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Paramètres

 _sz_
  
> [in] Pointeur vers la chaîne de caractères ASCII à partir de laquelle créer un identificateur d’entrée. 
    
 _carte de circuit imprimé_
  
> [out] Pointeur vers la taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _ppentry_ . 
    
 _ppentry_
  
> [out] Pointeur vers un pointeur vers la structure [ENTRYID](entryid.md) retournée qui contient l’identificateur d’entrée. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> La recréation a réussi.
    
MAPI_E_INVALID_ENTRYID
  
> L’identificateur d’entrée n’est pas valide.
    
## <a name="remarks"></a>Remarques

Les fonctions **HrEntryIDFromSz** et [HrSzFromEntryID](hrszfromentryid.md) fournissent la conversion entre les formats binaires d’identificateurs d’entrée de chaîne. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La fonction **HrEntryIDFromSz** alloue de la mémoire de la chaîne ASCII à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

