---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340963"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une restriction utilisée pour limiter un affichage de tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Paramètres

 _lpres_
  
> dans Structure [SRestriction](srestriction.md) définissant la restriction à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La restriction spécifiée, ou une ou plusieurs de ses sous-restrictions, n'est pas valide. 
    
FALSE 
  
> La restriction spécifiée et toutes ses sous-restrictions sont valides.
    
## <a name="remarks"></a>Remarques

Une fois qu'une restriction est validée, elle peut être transmise dans les appels à la méthode [IMAPITable:: Restrict](imapitable-restrict.md) pour limiter la table à certaines lignes, jusqu'à la méthode [IMAPITable:: FindRow](imapitable-findrow.md) pour localiser une ligne de table et aux méthodes de [IMAPIContainer](imapicontainerimapiprop.md) interface permettant d'effectuer une restriction sur un objet Container. 
  

