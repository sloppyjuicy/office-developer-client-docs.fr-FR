---
title: HrEntryIDFromSz
description: Cet article décrit la fonction HrEntryIDFromSz et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: 24c7c64ac54e64a479c783d5c710a4425245e051
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816884"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recrée un identificateur d’entrée à partir de son encodage ASCII. 
  
|Propriété |Valeur |
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

 _Sz_
  
> [in] Pointeur vers la chaîne ASCII à partir de laquelle créer un identificateur d’entrée. 
    
 _Pcb_
  
> [out] Pointeur vers la taille, en octets, de l’identificateur d’entrée pointé par le paramètre  _ppentry_ . 
    
 _ppentry_
  
> [out] Pointeur vers un pointeur vers la structure [ENTRYID](entryid.md) retournée qui contient le nouvel identificateur d’entrée. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Les loisirs ont réussi.
    
MAPI_E_INVALID_ENTRYID
  
> L’ID d’entrée n’était pas valide.
    
## <a name="remarks"></a>Remarques

Les fonctions **HrEntryIDFromSz** et [HrSzFromEntryID fournissent](hrszfromentryid.md) une conversion entre les formats de chaîne et binaire des identificateurs d’entrée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La fonction **HrEntryIDFromSz** alloue de la mémoire pour la chaîne ASCII à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

