---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8426f782eb5fbf8a125833c51b25ccd605acbd64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573522"
---
# <a name="szfindch"></a>SzFindCh
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Recherche la première occurrence d’un caractère dans une chaîne. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Paramètres

_lpsz_
  
> [in] Pointeur vers la chaîne à rechercher. 
    
_CH_
  
> [in] Le caractère à rechercher.
    
## <a name="return-value"></a>Valeur renvoy�e

**SzFindCh** retourne un pointeur vers la première occurrence du caractère de la chaîne. Si le caractère ne se produit pas n’importe où dans la chaîne, ou si le paramètre _lpsz_ est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La fonction **SzFindCh** cherche une correspondance exacte uniquement ; Il est sensible à la casse et différences diacritiques. Recherches dans les formats Unicode et DBCS sont pris en charge. 
  

