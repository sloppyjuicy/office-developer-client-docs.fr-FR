---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787442"
---
# <a name="upreade"></a>UPREADE

**S’applique à**: Outlook 
  
Obtenir des informations détaillées pour le téléchargement de l’état de lecture d’un élément pendant le [téléchargement lire l’état de l’état](upload-read-status-state.md).
  
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
- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPREAD](upread.md)

