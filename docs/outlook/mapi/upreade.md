---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fd593b68ef7ca25b1f8ceec613786cdbdd03fd76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579073"
---
# <a name="upreade"></a>UPREADE

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Obtenir des informations détaillées pour le téléchargement de l’état de lecture d’un élément pendant le [téléchargement lire l’état de l’état](upload-read-status-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
>  [out] / [in] indicateurs pour déterminer le comportement approprié lors du téléchargement. 
    
  - UPR_ASSOC
    
    - [out] L’élément est masqué.
    
  - UPR_READ
    
    - [out] L’état de lecture de l’élément a été modifié.
    
  - UPR_OK
    
    - [in] Téléchargement a réussi. Le client définit après le chargement des informations sur le serveur.
    
  - UPR_COMMIT
    
    - [in] Télécharger l’état de lecture de l’élément maintenant, au lieu d’attendre la fin de la [Télécharger l’état de la table](upload-table-state.md) pour le traitement par lots plusieurs éléments. 
    
_SKEY_
  
> [out] Clé de la source de l’élément.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPREAD](upread.md)

