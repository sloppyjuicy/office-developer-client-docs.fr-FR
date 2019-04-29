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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435389"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Alloue une mémoire tampon liée à une autre mémoire tampon précédemment allouée à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
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
  
> dans Taille, en octets, de la nouvelle mémoire tampon à allouer. 
    
 _lpObject_
  
> dans Pointeur vers un tampon MAPI existant alloué à l'aide de **MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> remarquer Pointeur vers la mémoire tampon renvoyée qui vient d'être allouée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé un pointeur vers la mémoire demandée.
    
## <a name="remarks"></a>Remarques

Pendant le traitement des appels **MAPIAllocateMore** , l'implémentation de l'appel acquiert un bloc de mémoire à partir du système d'exploitation. La mémoire tampon est allouée sur une adresse d'octet portant un numéro pair. Sur les plateformes où l'accès entier long est plus efficace, le système d'exploitation alloue la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre. 
  
La seule façon de libérer un tampon alloué avec **MAPIAllocateMore** est de transmettre le pointeur de mémoire tampon spécifié dans le paramètre _lpObject_ à la fonction [MAPIFreeBuffer](mapifreebuffer.md) . Le lien entre les mémoires tampons de mémoire allouées avec [MAPIAllocateBuffer](mapiallocatebuffer.md) et **MAPIAllocateMore** permet à **MAPIFreeBuffer** de libérer les deux tampons à l'aide d'un seul appel. 
  

