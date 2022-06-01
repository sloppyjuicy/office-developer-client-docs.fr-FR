---
title: MAPIAllocateMore
description: Décrit la fonction MAPIAllocateMore et fournit, la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
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
ms.openlocfilehash: 54e7e99f1ebe2a79f2332b765e7a54a0990b21de
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816128"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Alloue une mémoire tampon liée à une autre mémoire tampon précédemment allouée avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|Propriété |Valeur |
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
  
> [out] Pointeur vers la mémoire tampon retournée qui vient d’être allouée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a retourné un pointeur vers la mémoire demandée.
    
## <a name="remarks"></a>Remarques

Pendant le traitement des appels **MAPIAllocateMore** , l’implémentation d’appel acquiert un bloc de mémoire à partir du système d’exploitation. La mémoire tampon est allouée sur une adresse d’octet paire. Sur les plateformes où l’accès entier long est plus efficace, le système d’exploitation alloue la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre. 
  
La seule façon de libérer une mémoire tampon allouée avec **MAPIAllocateMore** consiste à passer le pointeur de mémoire tampon spécifié dans le paramètre _lpObject_ à la fonction [MAPIFreeBuffer](mapifreebuffer.md) . Le lien entre les mémoires tampons allouées avec [MAPIAllocateBuffer](mapiallocatebuffer.md) et **MAPIAllocateMore** permet à **MAPIFreeBuffer** de libérer les deux mémoires tampons avec un seul appel. 
  

