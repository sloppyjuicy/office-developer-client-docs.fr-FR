---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0075db0a515166c5185657daf3fc6b1e121d6672
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585121"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Recherche la première occurrence d’une sous-chaîne terminée dans une chaîne. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne à rechercher. Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères. 
    
 _lpszKey_
  
> [in] Pointeur vers la sous-chaîne terminée à rechercher. Le paramètre _lpszKey_ ne doit pas dépasser 65536 caractères. 
    
## <a name="return-value"></a>Valeur renvoy�e

 **SzFindSz** retourne un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne. Si la sous-chaîne ne se produit pas n’importe où dans la chaîne, si _lpszKey_ est supérieure à _lpsz_, ou si un paramètre est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La fonction **SzFindSz** cherche une correspondance exacte uniquement ; Il est sensible à la casse et différences diacritiques. Recherches dans des formats Unicode et DBCS sont pris en charge. La longueur maximale sur les deux paramètres est en caractères, pas nécessairement octets. 
  

