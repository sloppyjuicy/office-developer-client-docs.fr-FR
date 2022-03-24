---
title: FBadRestriction
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ddb8f3881f1b96d1a77fa0458c2a75d38eb67e19
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63716389"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une restriction utilisée pour limiter un affichage tableau. 
  
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
  
> La restriction spécifiée, ou une ou plusieurs de ses sous-sections, n’est pas valide. 
    
FALSE 
  
> La restriction spécifiée et toutes ses sous-sections sont valides.
    
## <a name="remarks"></a>Remarques

Une fois qu’une restriction est validée, elle peut être transmise dans des appels à la méthode [IMAPITable::Restrict](imapitable-restrict.md) pour limiter le tableau à certaines lignes, à la méthode [IMAPITable::FindRow](imapitable-findrow.md) pour localiser une ligne de tableau et aux méthodes de l’interface [IMAPIContainer](imapicontainerimapiprop.md) pour effectuer une restriction sur un objet conteneur. 
  

