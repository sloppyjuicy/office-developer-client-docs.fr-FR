---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c27fb4f9c95890bbffd72800b623dfc80cb559b8
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782306"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Réaffecte une mémoire tampon. Il est utilisé avec la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
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

 _lpv_
  
> Pointeur vers la mémoire à réaffecter.
    
 _ulSize_
  
> Taille, en octets, de la mémoire tampon à allouer.
    
 _lppv_
  
> Pointeur vers la mémoire tampon allouée renvoyée.
    
## <a name="remarks"></a>Remarques

 **MAPIReallocateBuffer** alloue un nouveau bloc de mémoire de la taille demandée et copie le contenu de la mémoire tampon qui est passée dans ce nouveau bloc de mémoire. Si le bloc de mémoire transmis contient des pointeurs internes, les pointeurs ne changent pas pour correspondre au nouvel emplacement. 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)

