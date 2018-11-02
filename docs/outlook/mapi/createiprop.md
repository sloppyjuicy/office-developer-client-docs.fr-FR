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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8d6eb011e65ad44f4183eb5821697dcf2508032c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566879"
---
# <a name="createiprop"></a>CreateIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet de données de propriété, autrement dit, un objet [IPropData](ipropdataimapiprop.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers un identificateur d’interface (IID) pour l’objet de données de propriété. L’identificateur d’interface valide est IID_IMAPIPropData. Passage de NULL dans le paramètre _lpInterface_ entraîne également l’objet de données de propriété retournée dans le paramètre _lppPropData_ pour effectuer un cast à l’interface standard pour un objet de données de propriété. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire. 
    
 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire. 
    
 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro. 
    
 _lppPropData_
  
> [out] Pointeur vers un pointeur vers l’objet de données de propriété retournées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface demandée n’est pas pris en charge pour cet objet.
    
## <a name="remarks"></a>Remarques

Les paramètres d’entrée _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ point [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), les fonctions [MAPIFreeBuffer](mapifreebuffer.md) , respectivement. Une application cliente appelant **CreateIProp** passe pointeurs aux fonctions MAPI nommées uniquement ; un fournisseur de services transmet les pointeurs vers ces fonctions qu’elle reçue dans son appel d’initialisation ou récupérés par un appel à la méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  

