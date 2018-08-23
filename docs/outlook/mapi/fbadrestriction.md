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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3d729e2a12ee19ee3aa4ded71263697eb739f154
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566305"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Valide une restriction utilisée pour limiter un affichage de tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Paramètres

 _lpres_
  
> [in] Une structure [SRestriction](srestriction.md) définissant la restriction à valider. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> La restriction spécifiée, ou un ou plusieurs de ses subrestrictions, ne sont pas valide. 
    
FALSE 
  
> La restriction spécifiée et tous ses subrestrictions sont valides.
    
## <a name="remarks"></a>Remarques

Une fois une restriction est validée, il peut être passé dans les appels à la méthode [IMAPITable](imapitable-restrict.md) pour restreindre la table à certaines lignes, la méthode [IMAPITable::FindRow](imapitable-findrow.md) pour localiser une ligne de tableau et aux méthodes de l' [IMAPIContainer](imapicontainerimapiprop.md) interface pour effectuer une restriction sur un objet conteneur. 
  

