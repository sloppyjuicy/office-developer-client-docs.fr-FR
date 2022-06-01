---
title: FBadRestriction
description: FBadRestriction valide une restriction utilisée pour limiter une vue de table. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
ms.openlocfilehash: f582133e899c11d1381ed7867a201ba212a197be
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816464"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une restriction utilisée pour limiter une vue de table. 
  
|Propriété |Valeur |
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
  
> [in] Structure [SRestriction](srestriction.md) définissant la restriction à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La restriction spécifiée, ou une ou plusieurs de ses sous-propriétés, n’est pas valide. 
    
FALSE 
  
> La restriction spécifiée et toutes ses sous-propriétés sont valides.
    
## <a name="remarks"></a>Remarques

Une fois qu’une restriction est validée, elle peut être passée dans les appels à la méthode [IMAPITable::Restrict pour restreindre](imapitable-restrict.md) la table à certaines lignes, à la méthode [IMAPITable::FindRow](imapitable-findrow.md) pour localiser une ligne de table et aux méthodes de l’interface [IMAPIContainer](imapicontainerimapiprop.md) pour effectuer une restriction sur un objet conteneur. 
  

