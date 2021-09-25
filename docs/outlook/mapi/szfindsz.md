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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 464c6ed3ce2c56339d38ec21648922618d1a4ad9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619644"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la première occurrence d’une sous-chaîne terminée par null dans une chaîne terminée par null. 
  
|||
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

 **SzFindSz** renvoie un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne. Si la sous-chaîne ne se produit nulle part dans la chaîne, si  _lpszKey_ est supérieur à  _lpsz_ ou si l’un des paramètres est NULL, une valeur NULL est renvoyée. 
  
## <a name="remarks"></a>Remarques

La **fonction SzFindSz** recherche une correspondance exacte uniquement ; il est sensible aux différences diacritiques et de cas. Les recherches au format Unicode et DBCS sont pris en charge. La limite de longueur pour les deux paramètres est en caractères, pas nécessairement en octets. 
  

