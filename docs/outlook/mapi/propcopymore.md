---
title: PropCopyMore
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 72113849508ee4b12b49d4008c649fc99b38e638
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725484"
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
  
 **PropCopyMore** n’a pas besoin d’allouer de mémoire, sauf si la valeur de propriété copiée est d’un type, tel que PT_STRING8, qui ne correspond pas à une structure [SPropValue](spropvalue.md) . Pour ces propriétés de grande taille, la fonction alloue de la mémoire à l’aide de la [fonction MAPIAllocateMore](mapiallocatemore.md) à laquelle un pointeur est transmis dans le paramètre _lpfAllocMore_ . 
  
Utilisationjudicious de la **mémoire des fragments PropCopyMore** ; envisagez plutôt [d’utiliser la fonction ScCopyProps](sccopyprops.md) . 
  

