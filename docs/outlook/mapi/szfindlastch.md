---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421255"
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

 **SzFindLastCh** renvoie un pointeur vers la dernière occurrence du caractère dans la chaîne. Si le caractère ne se produit nulle part dans la chaîne, ou si le paramètre  _lpsz_ est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La **fonction SzFindLastCh** recherche uniquement une correspondance exacte . il est sensible aux différences diacritiques et de cas. Les recherches dans les formats Unicode et DBCS sont pris en charge. 
  

