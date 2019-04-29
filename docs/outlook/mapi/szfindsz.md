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
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435221"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche la première occurrence d'une sous-chaîne terminée par un caractère NULL dans une chaîne terminée par un caractère null. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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
  
> dans Pointeur vers la chaîne terminée par un caractère null à rechercher. Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères. 
    
 _lpszKey_
  
> dans Pointeur vers la sous-chaîne terminée par un caractère null à rechercher. Le paramètre _lpszKey_ ne doit pas dépasser 65536 caractères. 
    
## <a name="return-value"></a>Valeur renvoyée

 **SzFindSz** renvoie un pointeur vers le premier caractère de la première occurrence de la sous-chaîne dans la chaîne. Si la sous-chaîne ne se produit nulle part dans la chaîne, si _lpszKey_ est supérieur à _lpsz_, ou si l'un des paramètres est NULL, la valeur null est renvoyée. 
  
## <a name="remarks"></a>Remarques

La fonction **SzFindSz** recherche une correspondance exacte uniquement; elle est sensible à la casse et aux différences diacritiques. Les recherches dans les formats Unicode et DBCS sont prises en charge. La limite de longueur sur les deux paramètres est exprimée en caractères, pas nécessairement en octets. 
  

