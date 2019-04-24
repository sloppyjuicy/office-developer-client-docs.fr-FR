---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333032"
---
# <a name="createiprop"></a>CreateIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de données de propriété, autrement dit, un objet [IPropData](ipropdataimapiprop.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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
  
> dans Pointeur vers un identificateur d'interface (IID) pour l'objet de données de propriété. L'identificateur d'interface valide est IID_IMAPIPropData. Le fait de transmettre NULL dans le paramètre _lpInterface_ entraîne également le cast de l'objet de données de propriété renvoyé dans le paramètre _lppPropData_ en interface standard pour un objet de données de propriété. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _lppPropData_
  
> remarquer Pointeur vers un pointeur vers l'objet de données de propriété renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L'interface demandée n'est pas prise en charge pour cet objet.
    
## <a name="remarks"></a>Remarques

Les paramètres d'entrée _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement. Une application cliente qui appelle **CreateIProp** passe des pointeurs vers les fonctions MAPI que vous venez de nommer; un fournisseur de services transmet les pointeurs à ces fonctions qu'il a reçues dans son appel d'initialisation ou qu'il a récupéré avec un appel à la méthode [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  

