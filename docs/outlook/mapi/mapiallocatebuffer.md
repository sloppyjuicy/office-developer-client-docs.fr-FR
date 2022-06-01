---
title: MAPIAllocateBuffer
description: Décrit la fonction MAPIAllocateBuffer et fournit, la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
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
ms.openlocfilehash: 2aba1d20e5a73f2ed764f7c6ad7c23f359a66a5e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812032"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Alloue une mémoire tampon. 
  
|Propriété|Valeur|
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
  
> [out] Pointeur vers la mémoire tampon allouée retournée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a retourné la mémoire tampon demandée.
    
## <a name="remarks"></a>Remarques

Pendant le traitement des appels **MAPIAllocateBuffer** , l’implémentation d’appel acquiert un bloc de mémoire à partir du système d’exploitation. La mémoire tampon est allouée sur une adresse d’octet paire. Sur les plateformes où l’accès entier long est plus efficace, le système d’exploitation alloue la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre. 
  
L’appel de la fonction [MAPIFreeBuffer](mapifreebuffer.md) libère la mémoire tampon allouée par **MAPIAllocateBuffer, en** appelant la fonction [MAPIAllocateMore](mapiallocatemore.md) et toutes les mémoires tampons qui lui sont liées, lorsque la mémoire n’est plus nécessaire. 
  
## <a name="see-also"></a>Voir aussi



[MAPIReallocateBuffer](mapireallocatebuffer.md)

