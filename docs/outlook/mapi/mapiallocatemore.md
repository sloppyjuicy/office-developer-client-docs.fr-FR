---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c0c69d3ed1960e372c9bd73a3822de1bc69b7de5
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462882"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Alloue une mémoire tampon liée à une autre mémoire tampon précédemment allouée avec la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers une mémoire tampon MAPI existante allouée à l’aide **de MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> [out] Pointeur vers la mémoire tampon nouvellement allouée renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé un pointeur vers la mémoire demandée.
    
## <a name="remarks"></a>Remarques

Pendant **le traitement des appels MAPIAllocateMore** , l’implémentation d’appel acquiert un bloc de mémoire du système d’exploitation. La mémoire tampon est allouée sur une adresse d’byte numérot e. Sur les plateformes où l’accès aux nombres longs est plus efficace, le système d’exploitation alloue la mémoire tampon à une adresse dont la taille en octets est un multiple de quatre. 
  
La seule façon de libérer une mémoire tampon **allouée avec MAPIAllocateMore** consiste à transmettre le pointeur de mémoire tampon spécifié dans le paramètre _lpObject_ à la fonction [MAPIFreeBuffer](mapifreebuffer.md) . Le lien entre les mémoires tampons de mémoire allouées avec [MAPIAllocateBuffer](mapiallocatebuffer.md) et **MAPIAllocateMore** permet à **MAPIFreeBuffer** de libérer les deux mémoires tampons avec un seul appel. 
  

