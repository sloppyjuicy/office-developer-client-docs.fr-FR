---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359422"
---
# <a name="uphier"></a>UPHIER
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour la synchronisation d'une hiérarchie de dossiers pendant l'état de la [hiérarchie de téléchargement](upload-hierarchy-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> dans Indicateurs permettant de modifier le comportement lors de la synchronisation de la hiérarchie de dossiers.
    
  - UPH_OK
    
    - dans Le chargement a réussi. Le client définit ceci après le chargement réussi des informations sur le serveur. À l'affichage de cet indicateur, Outlook efface toutes les informations de suivi internes qui indiquaient la hiérarchie de dossiers nécessaire à la mise à jour. 
    
    - Le client transmet le HRESULT si le chargement a échoué.
    
_pstmReserved_
  
> remarquer Ce membre est réservé à un usage interne d'Outlook et n'est pas pris en charge.
    
_iEnt_
  
> remarquer Index pour suivre la synchronisation du nombre de dossiers spécifiés par *cEnt* . 
    
_Motivé_
  
> remarquer Nombre de dossiers désynchronisés.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

