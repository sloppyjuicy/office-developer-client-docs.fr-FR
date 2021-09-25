---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c50f34f273f351bb0c2051247073cbc611013fd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579480"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Alloue une mémoire tampon. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Paramètres

 _cbSize_
  
> [in] Taille, en octets, de la mémoire tampon à allouer. 
    
 _lppBuffer_
  
> [out] Pointeur vers la mémoire tampon allouée renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la mémoire tampon demandée.
    
## <a name="remarks"></a>Remarques

Pendant le traitement des appels **MAPIAllocateBuffer,** l’implémentation d’appel acquiert un bloc de mémoire du système d’exploitation. La mémoire tampon est allouée sur une adresse d’byte numérot e. Sur les plateformes où l’accès aux nombres longs est plus efficace, le système d’exploitation alloue la mémoire tampon à une adresse dont la taille en octets est un multiple de quatre. 
  
L’appel de la fonction [MAPIFreeBuffer](mapifreebuffer.md) libère la mémoire tampon allouée par **MAPIAllocateBuffer**, en appelant la fonction [MAPIAllocateMore](mapiallocatemore.md) et toutes les mémoires tampons qui lui sont liées, lorsque la mémoire n’est plus nécessaire. 
  
## <a name="see-also"></a>Voir aussi



[MAPIReallocateBuffer](mapireallocatebuffer.md)

