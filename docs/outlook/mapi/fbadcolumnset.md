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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783289"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**S’applique à**: Outlook 
  
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
  

