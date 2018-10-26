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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577813"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère les adresses des mémoire allocation et libération de fonctions MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Paramètres

 _lppAllocateBuffer_
  
> [out] Pointeur vers un pointeur vers la fonction **MAPIAllocateBuffer** . **MAPIAllocateBuffer** alloue de la mémoire. 
    
 _lppAllocateMore_
  
> [out] Pointeur vers un pointeur vers la fonction **MAPIAllocateMore** . **MAPIAllocateMore** alloue de la mémoire supplémentaire pour la mémoire qui était alloué à l’aide de **MAPIAllocateBuffer**.
    
 _lppFreeBuffer_
  
> [out] Pointeur vers un pointeur vers la fonction **MAPIFreeBuffer** . **MAPIFreeBuffer** libère de la mémoire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les fonction adresses ont été correctement renvoyées.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::GetMemAllocRoutines** est implémentée pour tous les objets de prise en charge. Fournisseurs de services appellent **GetMemAllocRoutines** pour obtenir les adresses des fonctions d’allocation trois mémoire qui sont transmises à leur fonction d’initialisation ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

