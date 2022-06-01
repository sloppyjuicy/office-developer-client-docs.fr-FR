---
title: FBadColumnSet
description: FBadColumnSet teste la validité d’un jeu de colonnes de table à utiliser par un fournisseur de services dans un appel ultérieur à la méthode IMAPITableSetColumns.
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
ms.openlocfilehash: 66b2f726a105ad146767c894e92d31fca50f0d9e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817535"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Teste la validité d’un jeu de colonnes de table à utiliser par un fournisseur de services dans un appel ultérieur à la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
  
|Propriété |Valeur |
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
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété définissant les colonnes de table à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> L’ensemble de colonnes spécifié n’est pas valide. 
    
FALSE 
  
> L’ensemble de colonnes spécifié est valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadColumnSet** traite les colonnes de type PT_ERROR comme non valides et les colonnes de type PT_NULL comme valides. 
  

