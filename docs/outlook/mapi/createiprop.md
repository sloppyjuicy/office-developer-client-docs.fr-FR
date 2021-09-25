---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 510230c63eef41816fef29634365d11d2ab2cc42
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584660"
---
# <a name="createiprop"></a>CreateIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de données de propriété, c’est-à-dire un [objet IPropData.](ipropdataimapiprop.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers un identificateur d’interface (IID) pour l’objet de données de propriété. L’identificateur d’interface valide est IID_IMAPIPropData. La transmission de la valeur NULL dans le paramètre  _lpInterface_ entraîne également le cast de l’objet de données de propriété renvoyé dans le paramètre  _lppPropData_ vers l’interface standard d’un objet de données de propriété. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _lppPropData_
  
> [out] Pointeur vers un pointeur vers l’objet de données de propriété renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface demandée n’est pas prise en charge pour cet objet.
    
## <a name="remarks"></a>Remarques

Les paramètres d’entrée _lpAllocateBuffer,_ _lpAllocateMore_ et _lpFreeBuffer_ pointent respectivement vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer.](mapifreebuffer.md) Une application cliente appelant **CreateIProp** transmet des pointeurs vers les fonctions MAPI nommées ; un fournisseur de services transmet les pointeurs vers ces fonctions qu’il a reçues dans son appel d’initialisation ou récupérées avec un appel à la méthode [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  

