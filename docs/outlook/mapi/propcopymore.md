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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 635525a1c2c3234d724534d225eb07022afc9956
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592121"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Copie une seule valeur de propriété à partir d’un emplacement source vers un emplacement de destination. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [out] Pointeur vers l’emplacement sur lequel cette fonction écrit une structure [SPropValue](spropvalue.md) définissant la valeur de propriété copiées. 
    
 _lpSPropValueSrc_
  
> [in] Pointeur vers la structure [SPropValue](spropvalue.md) qui contient la valeur de propriété à copier. 
    
 _lpfAllocMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer plus de mémoire si l’emplacement de destination n’est pas suffisante pour contenir la propriété doit être copié. 
    
 _lpvObject_
  
> [in] Pointeur vers un objet pour lequel **MAPIAllocateMore** alloue de l’espace si nécessaire. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> La valeur de la propriété unique a été correctement copiée.
    
MAPI_E_NO_SUPPORT
  
> Un type de propriété inconnue s’est produite.
    
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services peut utiliser la fonction **PropCopyMore** pour copier une propriété en dehors d’une table qui doit être libéré pour pouvoir le pour utiliser ailleurs. 
  
 **PropCopyMore** n’a pas besoin d’allocation de mémoire, sauf si la valeur de la propriété copiée est d’un type, tel que PT_STRING8, qui ne rentre pas dans une structure [SPropValue](spropvalue.md) . Pour ces propriétés de grande taille, la fonction alloue de la mémoire à l’aide de la fonction [MAPIAllocateMore](mapiallocatemore.md) à laquelle un pointeur est passé dans le paramètre _lpfAllocMore_ . 
  
Injudicious utilisation de la mémoire de fragments de **PropCopyMore** ; envisager d’utiliser la fonction [ScCopyProps](sccopyprops.md) . 
  

