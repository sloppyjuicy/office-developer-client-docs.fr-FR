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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784730"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**S’applique à**: Outlook 
  
Affecte une mémoire tampon. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [out] Pointeur vers la mémoire tampon allouée retournée.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et a renvoyé la mémoire tampon de mémoire requise.
    
## <a name="remarks"></a>Remarques

Traitement des appels pendant **MAPIAllocateBuffer** , l’implémentation appelante acquiert un bloc de mémoire du système d’exploitation. La mémoire tampon est alloué sur une adresse de paires sur deux octets. Sur les plateformes où access entier long est plus efficace, le système d’exploitation alloue de la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre. 
  
Appel de la fonction de presse [MAPIFreeBuffer](mapifreebuffer.md) la mémoire tampon allouée par **MAPIAllocateBuffer**, en appelant la fonction [MAPIAllocateMore](mapiallocatemore.md) et les mémoires tampons liés, lorsque la mémoire n’est plus nécessaire. 
  
## <a name="see-also"></a>Voir aussi



[MAPIReallocateBuffer](mapireallocatebuffer.md)

