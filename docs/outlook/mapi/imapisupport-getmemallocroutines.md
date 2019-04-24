---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316558"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère les adresses des fonctions d'allocation et de désallocation de mémoire MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Paramètres

 _lppAllocateBuffer_
  
> remarquer Pointeur vers un pointeur vers la fonction **MAPIAllocateBuffer** . **MAPIAllocateBuffer** alloue de la mémoire. 
    
 _lppAllocateMore_
  
> remarquer Pointeur vers un pointeur vers la fonction **MAPIAllocateMore** . **MAPIAllocateMore** alloue de la mémoire supplémentaire pour la mémoire qui a été initialement allouée à l'aide de **MAPIAllocateBuffer**.
    
 _lppFreeBuffer_
  
> remarquer Pointeur vers un pointeur vers la fonction **MAPIFreeBuffer** . **MAPIFreeBuffer** libère de la mémoire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les adresses de la fonction ont été renvoyées avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: GetMemAllocRoutines** est implémentée pour tous les objets de prise en charge. Les fournisseurs de services appellent **GetMemAllocRoutines** pour obtenir les adresses des trois fonctions d'allocation de mémoire qui sont transmises à leur fonction d'initialisation ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

