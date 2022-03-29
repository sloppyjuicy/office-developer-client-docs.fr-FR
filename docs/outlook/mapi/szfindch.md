---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: Recherche la première occurrence d’un caractère dans une chaîne terminée par null. Les recherches dans les formats Unicode et DBCS sont pris en charge.
ms.openlocfilehash: 5594aaa3d514cd8e7bd1a4940cc21e42ee01b2fe
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456230"
---
# <a name="szfindch"></a>SzFindCh
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la première occurrence d’un caractère dans une chaîne terminée par null. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Paramètres

_lpsz_
  
> [in] Pointeur vers la chaîne terminée par null à rechercher. 
    
_ch_
  
> [in] Caractère à rechercher.
    
## <a name="return-value"></a>Valeur renvoyée

**SzFindCh renvoie** un pointeur vers la première occurrence du caractère dans la chaîne. Si le caractère ne se produit nulle part dans la chaîne, ou si le paramètre _lpsz_ est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La **fonction SzFindCh** recherche uniquement une correspondance exacte . il est sensible aux différences diacritiques et de cas. Les recherches dans les formats Unicode et DBCS sont pris en charge. 
  

