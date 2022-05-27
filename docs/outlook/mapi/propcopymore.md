---
title: PropCopyMore
description: Décrit PropCopyMore, qui copie une valeur de propriété unique d’un emplacement source vers un emplacement de destination.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
ms.openlocfilehash: e3f729eb85db97195ae3ab4fff457b6891d188ba
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752511"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une valeur de propriété unique d’un emplacement source vers un emplacement de destination. 
  
|Propriété |Valeur |
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
  
> [out] Pointeur vers l’emplacement dans lequel cette fonction écrit une structure [SPropValue](spropvalue.md) définissant la valeur de propriété copiée. 
    
 _lpSPropValueSrc_
  
> [in] Pointeur vers la structure [SPropValue](spropvalue.md) qui contient la valeur de propriété à copier. 
    
 _lpfAllocMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire si l’emplacement de destination n’est pas suffisamment grand pour contenir la propriété à copier. 
    
 _lpvObject_
  
> [in] Pointeur vers un objet pour lequel **MAPIAllocateMore** allouera de l’espace si nécessaire. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La valeur de propriété unique a été copiée avec succès.
    
MAPI_E_NO_SUPPORT
  
> Un type de propriété inconnu a été rencontré.
    
## <a name="remarks"></a>Remarques

Une application cliente ou un fournisseur de services peut utiliser la fonction **PropCopyMore** pour copier une propriété d’une table qui est sur le point d’être libérée afin de l’utiliser ailleurs. 
  
 **PropCopyMore** n’a pas besoin d’allouer de mémoire, sauf si la valeur de propriété copiée est d’un type, tel que PT_STRING8, qui ne tient pas dans une structure [SPropValue](spropvalue.md) . Pour ces grandes propriétés, la fonction alloue de la mémoire à l’aide de la fonction [MAPIAllocateMore](mapiallocatemore.md) à laquelle un pointeur est passé dans le paramètre _lpfAllocMore_ . 
  
Utilisation judicieuse de la mémoire des fragments **PropCopyMore** ; envisagez plutôt d’utiliser la fonction [ScCopyProps](sccopyprops.md) . 
  

