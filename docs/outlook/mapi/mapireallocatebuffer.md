---
title: MAPIReallocateBuffer
description: MAPIReallocateBuffer réalloue une mémoire tampon et elle est utilisée avec la fonction MAPIAllocateBuffer.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
ms.openlocfilehash: db3f318169af7a1585bedfece8e53847e873a6cc
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828240"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Réalloue une mémoire tampon. Il est utilisé avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |omapix.h  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Paramètres

 _Lpv_
  
> Pointeur vers la mémoire à réallouer.
    
 _ulSize_
  
> Taille, en octets, de la mémoire tampon à allouer.
    
 _lppv_
  
> Pointeur vers la mémoire tampon allouée retournée.
    
## <a name="remarks"></a>Remarques

 **MAPIReallocateBuffer alloue** un nouveau bloc de mémoire de la taille demandée et copie le contenu de la mémoire tampon passée dans ce nouveau bloc de mémoire. Si le bloc de mémoire transmis contient des pointeurs internes, les pointeurs ne changent pas pour correspondre au nouvel emplacement. 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)

