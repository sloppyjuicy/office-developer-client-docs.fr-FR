---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425693"
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

