---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: Recherche la première occurrence d’une sous-chaîne terminée par null dans une chaîne terminée par null. Les recherches dans les formats Unicode et DBCS sont pris en charge.
ms.openlocfilehash: 3e4cbd2120f572a40d9039d595903e31bd738fcc
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456223"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la première occurrence d’une sous-chaîne terminée par null dans une chaîne terminée par null. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne terminée par null à rechercher. Le  _paramètre lpsz_ ne doit pas dépasser 65 536 caractères. 
    
 _lpszKey_
  
> [in] Pointeur vers la sous-stration terminée par null à rechercher. Le  _paramètre lpszKey_ ne doit pas dépasser 65 536 caractères. 
    
## <a name="return-value"></a>Valeur renvoyée

 **SzFindSz** renvoie un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne. Si la sous-chaîne ne se produit pas dans la chaîne, si  _lpszKey_ est supérieur à  _lpsz_ ou si l’un des paramètres est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La **fonction SzFindSz** recherche uniquement une correspondance exacte . il est sensible aux différences diacritiques et de cas. Les recherches dans les formats Unicode et DBCS sont pris en charge. La limite de longueur pour les deux paramètres est en caractères, pas nécessairement en octets. 
  

