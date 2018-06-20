---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784768"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**S’applique à**: Outlook 
  
Réaffecte une mémoire tampon. Il est utilisé avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |omapix.h  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Paramètres

 _LPV_
  
> Pointeur vers la mémoire à être réaffecté.
    
 _ulSize_
  
> La taille, en octets, de la mémoire tampon à allouer.
    
 _lppv_
  
> Pointeur vers la mémoire tampon allouée retournée.
    
## <a name="remarks"></a>Remarques

 **MAPIReallocateBuffer** attribue un nouveau bloc de mémoire de la taille requise et copie le contenu de la mémoire tampon qui est passé dans ce nouveau bloc de mémoire. Si le bloc de mémoire est passée contient des pointeurs internes, les pointeurs ne modifiez pas pour correspondre au nouvel emplacement. 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)

