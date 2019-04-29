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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421941"
---
# <a name="szfindch"></a>SzFindCh
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la première occurrence d'un caractère dans une chaîne terminée par un caractère null. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
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
  
> dans Pointeur vers la chaîne terminée par un caractère null à rechercher. 
    
_ch_
  
> dans Caractère à rechercher.
    
## <a name="return-value"></a>Valeur renvoyée

**SzFindCh** renvoie un pointeur vers la première occurrence du caractère dans la chaîne. Si le caractère ne se produit nulle part dans la chaîne, ou si le paramètre _lpsz_ est null, la valeur null est renvoyée. 
  
## <a name="remarks"></a>Remarques

La fonction **SzFindCh** recherche une correspondance exacte uniquement; elle est sensible à la casse et aux différences diacritiques. Les recherches dans les formats Unicode et DBCS sont prises en charge. 
  

