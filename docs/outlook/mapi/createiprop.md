---
title: CreateIProp
description: CreateIProp crée un objet de données de propriété, c’est-à-dire un objet IPropData. Cet article décrit ses paramètres, sa valeur de retour et ses remarques.
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
ms.openlocfilehash: 4615e55429733f0e4f03bed6673ac04e42b72901
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816961"
---
# <a name="createiprop"></a>CreateIProp

**S’applique à** : Outlook 2013 | Outlook 2016
  
Crée un objet de données de propriété, [c’est-à-dire un objet IPropData](ipropdataimapiprop.md) .
  
|Propriété|Valeur|
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
  
> [in] Pointeur vers un identificateur d’interface (IID) pour l’objet de données de propriété. L’identificateur d’interface valide est IID_IMAPIPropData. Le passage de NULL dans le paramètre _lpInterface_ entraîne également le cast de l’objet de données de propriété retourné dans le paramètre _lppPropData_ vers l’interface standard pour un objet de données de propriété.

 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.

 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer de la mémoire supplémentaire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.

 _lpvReserved_
  
> [in] R�serv� ; doit �tre �gal � z�ro.

 _lppPropData_
  
> [out] Pointeur vers un pointeur vers l’objet de données de propriété retourné.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_INTERFACE_NOT_SUPPORTED
  
> L’interface demandée n’est pas prise en charge pour cet objet.

## <a name="remarks"></a>Remarques

Les paramètres d’entrée _lpAllocateBuffer_, _lpAllocateMore_ et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md) et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement. Une application cliente appelant **CreateIProp** transmet des pointeurs aux fonctions MAPI qui viennent d’être nommées ; un fournisseur de services transmet les pointeurs à ces fonctions qu’il a reçues dans son appel d’initialisation ou récupérées avec un appel à la méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .
  