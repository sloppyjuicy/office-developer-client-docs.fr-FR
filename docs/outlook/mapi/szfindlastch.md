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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787322"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**S’applique à**: Outlook 
  
Recherche la dernière occurrence d’un caractère dans une chaîne. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **SzFindLastCh** retourne un pointeur vers la dernière occurrence du caractère de la chaîne. Si le caractère ne se produit pas n’importe où dans la chaîne, ou si le paramètre _lpsz_ est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La fonction **SzFindLastCh** cherche une correspondance exacte uniquement ; Il est sensible à la casse et différences diacritiques. Recherches dans les formats Unicode et DBCS sont pris en charge. 
  

