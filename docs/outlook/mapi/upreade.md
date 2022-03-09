---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
ms.openlocfilehash: 5d42b6ba42b7a5a87185c981fc53ddb87cca3820
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379590"
---
# <a name="upreade"></a>UPREADE

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations étendues pour le chargement de l’état de lecture d’un élément pendant l’état de [lecture du chargement](upload-read-status-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> [out]/[in] Indicateurs pour déterminer le comportement approprié pendant le chargement. 
    
  - UPR_ASSOC
    
    - [out] L’élément est masqué.
    
  - UPR_READ
    
    - [out] L’état de lecture de l’élément a été modifié.
    
  - UPR_OK
    
    - [in] Télécharger a réussi. Le client définit cette information après le téléchargement d’informations sur le serveur.
    
  - UPR_COMMIT
    
    - [in] Télécharger l’état de lecture de l’élément maintenant, au lieu d’attendre la fin de l’état de [la table](upload-table-state.md) de chargement pour traiter par lots plusieurs éléments. 
    
_skey_
  
> [out] Clé source de l’élément.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPREAD](upread.md)

