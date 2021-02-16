---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404469"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une valeur de propriété unique d’un emplacement source vers un emplacement de destination. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValueDest_
  
> [out] Pointeur vers l’emplacement auquel cette fonction écrit une structure [SPropValue](spropvalue.md) définissant la valeur de la propriété copiée. 
    
 _lpSPropValueSrc_
  
> [in] Pointeur vers la structure [SPropValue](spropvalue.md) qui contient la valeur de propriété à copier. 
    
 _lpfAllocMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire si l’emplacement de destination n’est pas assez grand pour contenir la propriété à copier. 
    
 _lpvObject_
  
> [in] Pointeur vers un objet pour lequel **MAPIAllocateMore alloue** de l’espace si nécessaire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La valeur de propriété unique a été correctement copiée.
    
MAPI_E_NO_SUPPORT
  
> Un type de propriété inconnu a été rencontré.
    
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services peut utiliser la fonction **PropCopyMore** pour copier une propriété d’une table qui est sur le point d’être libérée afin de l’utiliser ailleurs. 
  
 **PropCopyMore** n’a pas besoin d’allouer de mémoire, sauf si la valeur de propriété copiée est d’un type, tel que PT_STRING8, qui ne correspond pas à une structure [SPropValue.](spropvalue.md) Pour ces propriétés de grande taille, la fonction alloue de la mémoire à l’aide de la [fonction MAPIAllocateMore](mapiallocatemore.md) à laquelle un pointeur est transmis dans le paramètre _lpfAllocMore._ 
  
Utilisationjudicious de la mémoire des fragments **PropCopyMore** ; envisagez plutôt d’utiliser la fonction [ScCopyProps.](sccopyprops.md) 
  

