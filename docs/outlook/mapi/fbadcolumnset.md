---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1498705c0459798f1ae8c49586423603500c6e8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601001"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Teste la validité d’un ensemble de colonnes de tableau à utiliser par un fournisseur de services dans un appel ultérieur à la méthode [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Paramètres

 _lpptaCols_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété définissant les colonnes de tableau à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Le jeu de colonnes spécifié n’est pas valide. 
    
FALSE 
  
> Le jeu de colonnes spécifié est valide.
    
## <a name="remarks"></a>Remarques

La **fonction FBadColumnSet** traite les colonnes de type PT_ERROR comme non valides et les colonnes de type PT_NULL comme valides. 
  

