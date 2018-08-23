---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575097"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La validité d’une colonne de table définie pour les tests utilisent par un fournisseur de services dans un appel suivant à la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Paramètres

 _lpptaCols_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété définir les colonnes de la table à valider. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> L’ensemble de la colonne spécifiée n’est pas valide. 
    
FALSE 
  
> L’ensemble de la colonne spécifiée est valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadColumnSet** traite les colonnes du type PT_ERROR comme non valide et les colonnes du type PT_NULL comme étant valide. 
  

