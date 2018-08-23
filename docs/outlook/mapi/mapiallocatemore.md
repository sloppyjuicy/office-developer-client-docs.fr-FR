---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0e6226dd0fc9c04070ed3d1dda1770f77fbc585c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583007"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Affecte une mémoire tampon qui est liée à une autre mémoire tampon précédemment allouée avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Paramètres

 _cbSize_
  
> [in] Taille, en octets, de la nouvelle mémoire tampon à allouer. 
    
 _lpObject_
  
> [in] Pointeur vers un tampon MAPI existant alloué à l’aide de **MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> [out] Pointeur vers retourné nouvellement allouer de la mémoire tampon.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et a renvoyé un pointeur vers la mémoire requise.
    
## <a name="remarks"></a>Remarques

Traitement des appels pendant **MAPIAllocateMore** , l’implémentation appelante acquiert un bloc de mémoire du système d’exploitation. La mémoire tampon est alloué sur une adresse de paires sur deux octets. Sur les plateformes où access entier long est plus efficace, le système d’exploitation alloue de la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre. 
  
Le seul moyen pour libérer la mémoire tampon allouée avec **MAPIAllocateMore** consiste à passer le pointeur de la mémoire tampon spécifié dans le paramètre _lpObject_ à la fonction [MAPIFreeBuffer](mapifreebuffer.md) . La liaison entre les mémoire tampon allouée avec [MAPIAllocateBuffer](mapiallocatebuffer.md) et **MAPIAllocateMore** active **MAPIFreeBuffer** libérer les deux tampons avec un seul appel. 
  

