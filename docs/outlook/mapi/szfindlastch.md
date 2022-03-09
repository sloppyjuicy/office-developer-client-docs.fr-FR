---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a939a7cf06370d5306d1f6a3bada850909897064
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465456"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la dernière occurrence d’un caractère dans une chaîne terminée par null. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **SzFindLastCh** renvoie un pointeur vers la dernière occurrence du caractère dans la chaîne. Si le caractère ne se produit nulle part dans la chaîne, ou si le paramètre _lpsz_ est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La **fonction SzFindLastCh** recherche uniquement une correspondance exacte . il est sensible aux différences diacritiques et de cas. Les recherches dans les formats Unicode et DBCS sont pris en charge. 
  

